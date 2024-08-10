<script>
	import Header from '../../components/Header.svelte';
	import Prose from '../../components/Prose.svelte';
	import StyleLink from '../../components/StyleLink.svelte';
</script>

<Header />

<div class="m-4 font-mono">
	<StyleLink classDefs="text-xl" url="https://github.com/arnavsurve/vcs">
		vcs (july 2024 - aug 2024)
	</StyleLink>

	<Prose classDefs="p-2">
		A version control system written in Go with the Cobra library for creating CLI applications,
		using SHA1 hashes to track changes in files and directories. This project was created as an
		exercise in Go development and for a deeper understanding of how version control systems work.
		This is essentially a simplified version of Git with a subset of its features, inspired by <StyleLink
			url="https://ryanheathcote.com/git/build-your-own-vcs">Build Your Own VCS</StyleLink
		> by Ryan Heathcote. Code hosted on GitHub at the link above.
	</Prose>

	<br />

	<StyleLink classDefs="text-xl" url="https://github.com/arnavsurve/lastfm-crawl">
		lastfm-crawl (july 2024)
	</StyleLink>

	<Prose classDefs="p-2">
		HTML embed solutions for Last.fm stats suck - they are either not customizable, slow, or most of
		the time both. I wanted to create a performant, customizable, and versatile solution for
		embedding Last.fm stats on my website at <StyleLink url="/misc">/misc</StyleLink>; the goal
		being to provide endpoints that returned raw metrics in JSON, allowing the developer to display
		data in the frontend as they wish. This is a wrapper for the <StyleLink
			url="https://www.last.fm/home">last.fm</StyleLink
		> API written in Python (Flask), containerized with Docker, and hosted with AWS Lambda for personal
		use. Additionally, I utilize Zappa to provide a CI/CD pipeline for seamless testing and deployment.
		Code hosted on GitHub at the link above.
	</Prose>

	<br />

	<div>
		<StyleLink classDefs="text-xl" url="https://github.com/arnavsurve/website">
			surve.dev (july 2024)
		</StyleLink>
		<Prose classDefs="p-2">
			My personal website built using SvelteKit for the frontend UI and TailwindCSS for styling
			components and using Vercel to provide a CI/CD pipeline for deployment and hosting. The design
			of this website is inspired by the <StyleLink url={'https://tinygrad.org/'}
				>tinygrad</StyleLink
			> website. Code hosted on GitHub at the link above.
		</Prose>
	</div>

	<br />

	<div>
		<StyleLink classDefs="text-xl" url="https://github.com/arnavsurve/md-preview">
			md-preview (may 2024)
		</StyleLink>
		<Prose classDefs="p-2">
			I wanted a lightweight solution to preview markdown files in the browser over localhost. This
			is an implementation using Node.js to serve an HTML page that renders markdown syntax with
			custom styling tailored to my preferences. Code hosted on GitHub at the link above.
		</Prose>

		<br />

		<img src="/mdprev.png" alt="md-preview" class="xs:w-full sm:w-full md:w-2/3 lg:w-1/2" />
	</div>
</div>
