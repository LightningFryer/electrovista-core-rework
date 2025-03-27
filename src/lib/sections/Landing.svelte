<script>
	import { goto } from '$app/navigation';
	import gsap from 'gsap';
	import { onMount } from 'svelte';

	// import Marqueeck from "@arisbh/marqueeck";
	// import Marquee from 'svelte-fast-marquee';

	onMount(() => {
		gsap.from('.landing-club-dep-logos', {
			duration: 0.5,
			stagger: 0.2,
			opacity: 0,
			scale: 1.5
		});
	});
</script>

<main
	class="dotted-background-wrapper flex h-screen flex-col items-center justify-center !bg-black"
>
	<div class="text-default-text mt-20 flex h-full w-full flex-col items-center justify-center">
		<img src="src\lib\images\elec.png" alt="electrovista_logo" class="h-72" />

		<button class="btn btn-lg cursor-pointer rounded-full">Scroll on to see more!</button>
	</div>
</main>

<style>
	.dotted-background-wrapper {
		background-color: transparent;
		background: radial-gradient(circle, rgb(22, 22, 22) 10%, transparent 1%) 0 0 / 20px 20px;
		background-size: 35px 35px; /* !!!!!THIS SHOULD BE SAME AS THE BACKGROUND POSITION CELL SIZE IN THE KEYFRAME OTHERWISE YOU'LL SEE HORRIBLE STUTTERING!!!!! */
		animation: moveLeft 2s linear infinite;
	}

	@keyframes moveLeft {
		0% {
			background-position: 0 0;
		}
		100% {
			background-position: 35px -35px; /* Moves by exactly one grid cell size */
		}
	}
</style>
