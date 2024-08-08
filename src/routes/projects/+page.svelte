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
		This is a version control system written in Go with the Cobra library for creating CLI applications.
		This project was created as a learning experience for Go and for a deeper understanding of how version control systems work.
		The goal was to create a simple and perfomant
		version control system that could be used to track file and directory changes. The project is essentially a simplified version 
		of Git with a subset of its features. Inspired by <StyleLink url="https://github.com/git/git">Git</StyleLink> and 
		<StyleLink url="https://ryanheathcote.com/git/build-your-own-vcs">Build Your Own VCS</StyleLink> by Ryan Heathcote, a Bash implementation 
		of this project. Code is hosted on GitHub at the link above.
	</Prose>

	<br />

	<StyleLink classDefs="text-xl" url="https://github.com/arnavsurve/lastfm-crawl">
		lastfm-crawl (july 2024)
	</StyleLink>

	<Prose classDefs="p-2">
		HTML embed solutions for Last.fm stats suck - they are either not customizable, slow, or most of
		the time both. I wanted to create a performant, customizable, and versatile solution for
		embedding Last.fm stats on my website at <StyleLink url="/misc">/misc</StyleLink>. This is a
		wrapper for the <StyleLink url="https://www.last.fm/home">last.fm</StyleLink> API written in Python
		(Flask), containerized with Docker, and hosted with AWS Lambda for personal use. The goal was to
		provide endpoints that only returned JSON, allowing the developer to display data in the frontend
		as they wish. Code hosted on GitHub at the link above.
	</Prose>

	<br />

	<div>
		<StyleLink classDefs="text-xl" url="https://github.com/arnavsurve/website">
			this website (july 2024)
		</StyleLink>
		<Prose classDefs="p-2">
			This is my personal website built using SvelteKit for the frontend UI and TailwindCSS for
			styling components. The source code is available on GitHub at the link above, and I am using
			Vercel for deployment and hosting. The design of this website is inspired by the <StyleLink
				url={'https://tinygrad.org/'}>tinygrad</StyleLink
			> website.
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
