<script>
	import Header from '../components/Header.svelte';
	import Prose from '../components/Prose.svelte';
	import StyleLink from '../components/StyleLink.svelte';
</script>

<Header />

<div class="m-4 font-mono sm:flex md:flex lg:flex justify-between">
	<div class="m-2">
		<div class="xs:w-1/2 sm:w-2/5 lg:w-1/4 xl:w-1/5">
			<img src="/tinyboxes.png" alt="tinyboxes" class="" />
		</div>

		<br />

		<Prose>
			I am a third-year student at California State University, Sacramento pursuing a BS in Computer
			Science. Passionate about everything software and a relentless advocate for open-source
			software and the Linux community. Open to software development and sysadmin opportunities.
			<br /><br />
			Linux sysadmin and DevOps engineering have been of recent key interest to me. I have been working
			through this <StyleLink url="https://roadmap.sh/devops">DevOps Roadmap</StyleLink> and studying
			for the
			<StyleLink url="https://aws.amazon.com/certification/certified-solutions-architect-associate/"
				>AWS Certified Solutions Architect - Associate</StyleLink
			> certification.
			<br /><br />
			Currently focused on developing a strong foundation in Go and Python programming as well as gaining
			hands-on sysadmin experience with a homelab Ubuntu server environment on an old 2017 Macbook Pro.
			I have ~2 years experience with both Debian (apt) and RHEL (dnf/yum) based linux distributions.
		</Prose>

		<br />

		<div class="font-mono">
			<h1 class="text-xl">this summer I am:</h1>
			<ul class="text-sm list-disc p-2">
				<li>Interning with MITER Brands IT Infrastructure in Tacoma, WA</li>
				<li>Conducting infrasound research under the NASA California Space Grant Consortium</li>
				<li>Taking MATH410 (Intro to Linear Algebra) at American River College</li>
			</ul>
		</div>
	</div>
</div>
