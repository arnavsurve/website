<script>
	import Header from '../components/Header.svelte';
	import Prose from '../components/Prose.svelte';
	import StyleLink from '../components/StyleLink.svelte';
</script>

<Header />

<div class="m-4 font-mono sm:flex md:flex lg:flex justify-between">
	<div class="m-2">
		<!-- <div class="xs:w-1/2 sm:w-3/5 lg:w-1/2 xl:w-2/5 2xl:w-2/6"> -->
		<!-- 	<img src="/humor.jpeg" alt="tinyboxes" class="" /> -->
		<!-- </div> -->
		<!---->
		<!-- <br /> -->

		<Prose>
			I'm a third-year student at CSU Sacramento pursuing a BS in Computer Science. I like
			administrating servers and building web apps in my free time.
			<br /><br />
			Currently working on a project called
			<a href="https://github.com/EaRu723/ynot.lol-web" class="underline">Y</a>, connecting users
			and multimedia across the web using the
			<a href="https://atproto.com/" class="underline">AT Protocol</a>.
			<br /><br />
		</Prose>

		<br />

		<!-- <div class="font-mono"> -->
		<!-- 	<h1 class="text-xl">this summer I:</h1> -->
		<!-- 	<ul class="text-sm list-disc p-2"> -->
		<!-- 		<li>Interned with MITER Brands IT Infrastructure in Tacoma, WA</li> -->
		<!-- 		<li>Conducted infrasound research under the NASA California Space Grant Consortium</li> -->
		<!-- 		<li>Took MATH410 (Intro to Linear Algebra) at American River College</li> -->
		<!-- 	</ul> -->
		<!-- </div> -->
	</div>
</div>
