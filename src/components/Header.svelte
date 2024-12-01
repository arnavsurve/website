<script>
	import { onMount } from 'svelte';
	import Navbar from './Navbar.svelte';

	onMount(() => {
		const name = document.getElementById('name');
		const text = 'arnav surve';
		let i = 0;
		const type = () => {
			if (i < text.length) {
				// @ts-ignore
				name.innerHTML += text.charAt(i);
				i++;
				setTimeout(type, 70);
			}
		};
		type();
	});
</script>

<div class="font-mono p-4">
	<div>
		<h1 id="name" class="text-slate-500 text-3xl blinking-cursor justify-start"></h1>
	</div>

	<div class="w-full py-2">
		<a class="hover:underline" href="mailto:arnav@surve.dev">arnav@surve.dev</a>
		<a class="hover:underline" href="https://www.github.com/arnavsurve">github</a>
		<a class="hover:underline" href="https://www.linkedin.com/in/arnavsurve/">linkedin</a>
	</div>
</div>

<hr class="mx-4" />
<!-- <Navbar /> -->

<style>
	@keyframes blink {
		0%,
		100% {
			opacity: 0;
		}
		50% {
			opacity: 1;
		}
	}

	.blinking-cursor::after {
		content: '_';
		animation: blink 1.5s step-start infinite;
		font-weight: bold;
	}

	h1 {
		display: inline-block; /* Allows the cursor to appear right after the text */
	}
</style>
