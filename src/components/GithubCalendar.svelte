<script>
	import { onMount } from 'svelte';
	import ActivityCalendarWidget from 'activity-calendar-widget/svelte';
	import { PUBLIC_GITHUB_PAT } from '$env/static/public';

	let data = [];

	const loadGithubActivity = async () => {
		const githubId = 'arnavsurve';
		const token = PUBLIC_GITHUB_PAT;

		const query = `
    		  query ($username: String!, $from: DateTime!, $to: DateTime!) {
    		    user(login: $username) {
    		      contributionsCollection(from: $from, to: $to) {
    		        contributionCalendar {
    		          weeks {
    		            contributionDays {
    		              date
    		              contributionCount
    		            }
    		          }
    		        }
    		      }
    		    }
    		  }
    		`;

		const today = new Date();
		const lastYear = new Date(today);
		lastYear.setFullYear(today.getFullYear() - 1);

		const variables = {
			username: githubId,
			from: lastYear.toISOString(),
			to: today.toISOString()
		};

		const response = await fetch('https://api.github.com/graphql', {
			method: 'POST',
			headers: {
				'Content-Type': 'application/json',
				Authorization: `Bearer ${token}`
			},
			body: JSON.stringify({ query, variables })
		});

		const result = await response.json();

		if (result.errors) {
			console.error('Error fetching GitHub data:', result.errors);
			return;
		}

		const weeks = result.data.user.contributionsCollection.contributionCalendar.weeks;
		const eventObj = {};

		weeks.forEach((week) => {
			week.contributionDays.forEach((day) => {
				const date = day.date;
				const count = day.contributionCount;
				if (count > 0) {
					eventObj[date] = Array(count).fill({ type: 'Contribution' });
				}
			});
		});

		data = Object.entries(eventObj).map(([date, activities]) => ({
			date,
			activities
		}));
	};

	onMount(() => {
		loadGithubActivity();
	});
</script>

<div>
	<ActivityCalendarWidget daysToRender={200} {data} levelColorMode="light" />
</div>

<style>
	img {
		width: 82px;
	}
</style>
