<script>
	import { onMount } from 'svelte';
	import ActivityCalendarWidget from 'activity-calendar-widget/svelte';
	import { PUBLIC_GITHUB_PAT } from '$env/static/public';

	let data = [];
	let totalCommits2024 = 0; // Variable to store 2024 contributions
	let summaryText = '';

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
		totalCommits2024 = 0; // Reset count

		weeks.forEach((week) => {
			week.contributionDays.forEach((day) => {
				const date = day.date;
				const count = day.contributionCount;
				if (count > 0) {
					eventObj[date] = Array(count).fill({ type: 'Contribution' });

					// Check if the date is in 2024
					const year = new Date(date).getFullYear();
					if (year === 2024) {
						totalCommits2024 += count; // Add to 2024 count
					}
				}
			});
		});

		data = Object.entries(eventObj).map(([date, activities]) => ({
			date,
			activities
		}));

		// Update the summary text dynamically
		summaryText = `${totalCommits2024} commits in 2024`;
	};

	onMount(() => {
		loadGithubActivity();
	});
</script>

<div>
	<ActivityCalendarWidget
		daysToRender={200}
		{data}
		levelColorMode="light"
		showLevels={false}
		{summaryText}
	/>
</div>

<style>
	img {
		width: 82px;
	}
</style>
