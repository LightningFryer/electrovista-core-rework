<script>
	import { blobStoreUrl } from '$lib/blobStoreUrl';
	import gsap from 'gsap';
	import { onMount } from 'svelte';

	onMount(() => {
		gsap
			.from('.elec-main-text', {
				duration: 1.5,
				opacity: 0,
				scale: 0,
				ease: 'back.out'
			})
			.then(() => {
				gsap
					.to('.landing-main-logo', {
						duration: 1,
						opacity: 1,
						ease: 'back.out'
					})
					.then(() => {
						gsap.to('.landing-main-logo', {
							duration: 60,
							repeat: -1,
							rotation: '360',
							ease: 'none'
						});
					});
			});
	});
</script>

<main
	class="dotted-background-wrapper flex h-screen flex-col items-center justify-center !bg-[#171717]"
	id="landing-sec"
>
	<div
		class="text-default-text mt-20 flex h-full w-full flex-col items-center justify-center gap-y-6"
	>
		<div class="flex flex-row items-center justify-center">
			<h1
				class="elec-main-text font-league-gothic text-[4rem] font-semibold text-white md:ml-20 md:text-[10rem]"
			>
				ELECTR
			</h1>
			<!-- This div is to add space between the ELECTRO, LOGO, VISTA-->
			<div class="mr-10 ml-10 md:mr-20 md:ml-20"></div>

			<img
				src={`${blobStoreUrl}/images/logos/elec_base_logo.png`}
				alt="electrovista_logo"
				class="landing-main-logo absolute z-10 mb-3 ml-4 h-32 overflow-scroll opacity-0 md:mb-3 md:ml-0 md:h-80"
			/>

			<h1
				class="elec-main-text font-league-gothic text-[4rem] font-semibold text-white md:mr-[7rem] md:text-[10rem]"
			>
				VISTA!
			</h1>
		</div>
		<h2 class="font-kanit text-lg font-semibold text-white md:text-2xl">
			OFFICIAL ECE CLUB OF <span class="text-[#ac533c]">MITBLR</span>
		</h2>
		<button
			class="btn btn-lg font-kanit mt-6 cursor-pointer rounded-full font-light shadow-none hover:border-[#3A6351] hover:bg-[#3A6351] hover:text-white"
			>Scroll on to see more!</button
		>
	</div>
</main>

<style>
	.dotted-background-wrapper {
		background-color: transparent;
		background: radial-gradient(circle, #444444 10%, transparent 1%) 0 0 / 20px 20px;
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
