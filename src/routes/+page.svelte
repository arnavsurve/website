<script>
	import Header from '../components/Header.svelte';
	import Prose from '../components/Prose.svelte';
	import StyleLink from '../components/StyleLink.svelte';
</script>

<Header />

<div class="m-4 font-mono sm:flex md:flex lg:flex justify-between">
	<div class="m-2">
		<div class="xs:w-1/2 sm:w-3/5 lg:w-1/2 xl:w-2/5 2xl:w-2/6">
			<img src="/portainer.png" alt="tinyboxes" class="" />
		</div>

		<br />

		<Prose>
			I'm a third-year student at California State University, Sacramento pursuing a BS in Computer
			Science. Passionate about everything software and a relentless advocate for open-source
			software and the Linux community. Open to SWE and adjacent opportunities.
			<br /><br />
			Server-side development and DevOps engineering have been of recent key interest to me. I have been working
			through this <StyleLink url="https://roadmap.sh/devops">DevOps Roadmap</StyleLink> and studying
			for the
			<StyleLink url="https://aws.amazon.com/certification/certified-solutions-architect-associate/"
				>AWS Certified Solutions Architect - Associate</StyleLink
			> certification.
			<br /><br />
			Currently focused on skilling up my Go programming as well as gaining
			hands-on hardware sysadmin and CI/CD experience on a homelab setup.
			I have ~2 years experience with Debian based linux distributions and have a CentOS box sitting somewhere in my closet as well.
		</Prose>

		<br />

		<div class="font-mono">
			<h1 class="text-xl">this summer I:</h1>
			<ul class="text-sm list-disc p-2">
				<li>Interned with MITER Brands IT Infrastructure in Tacoma, WA</li>
				<li>Conducted infrasound research under the NASA California Space Grant Consortium</li>
				<li>Took MATH410 (Intro to Linear Algebra) at American River College</li>
			</ul>
		</div>
	</div>
</div>
