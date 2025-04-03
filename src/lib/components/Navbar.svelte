<script lang="ts">
	import { goto } from '$app/navigation';
	import { onMount } from 'svelte';
	import Navrail from './Navrail.svelte';
	let openNavrailComponent = false;
	import gsap from 'gsap';
	import { blobStoreUrl } from '$lib/blobStoreUrl';

	let navBarLogoRotateAnim: GSAPTween;

	onMount(() => {
		navBarLogoRotateAnim = gsap.to('.navbar-icon', {
			repeat: -1,
			rotation: '360',
			duration: 5,
			ease: 'none',
			paused: true
		});
	});
</script>

<nav
	class="fixed z-20 flex h-20 max-w-screen min-w-screen justify-between bg-[#3A6351]/80 shadow-2xl shadow-black"
>
	<div class="flex flex-col">
		<!-- svelte-ignore a11y_no_static_element_interactions -->
		<!-- svelte-ignore a11y_click_events_have_key_events -->
		<div
			class="flex h-full w-full flex-row items-center justify-start pl-6"
			onmouseenter={() => (openNavrailComponent = true)}
			onmouseleave={() => (openNavrailComponent = false)}
			onclick={() => !openNavrailComponent}
		>
			<!-- <a
				href="/"
				class="navbar-logo btn btn-circle size-16 rounded-full border-none bg-white p-6 text-black transition-[scale] duration-300 hover:scale-105 hover:bg-yellow-300 hover:text-white"
				></a
			> -->
			<div
				class="navbar-icon flex flex-col items-center justify-center"
				onmouseenter={() => navBarLogoRotateAnim.resume()}
				onmouseleave={() => {
					navBarLogoRotateAnim.restart();
					navBarLogoRotateAnim.pause();
				}}
			>
				<img
					src={`${blobStoreUrl}/images/logos/elec_base_logo.png`}
					class="btn btn-circle btn-xl border-[#3A6351] shadow-none"
					alt="navbar_logo"
				/>
			</div>
		</div>
		<div><Navrail navrailOpen={openNavrailComponent} /></div>
	</div>
	<div>
		<img
			src={`${blobStoreUrl}/images/logos/manipal_logo.png`}
			class="invisible max-h-16 md:visible md:mt-2 md:mr-6"
			alt="manipal_logo"
		/>
	</div>
</nav>
