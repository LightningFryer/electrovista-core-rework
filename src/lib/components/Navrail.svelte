<script>
	let { navrailOpen = false } = $props();
	import gsap from 'gsap';
	import { ScrollToPlugin } from 'gsap/ScrollToPlugin';
	import { onMount } from 'svelte';

	onMount(() => {
		gsap.registerPlugin(ScrollToPlugin);
	});

	const scrollToHome = () => {
		gsap.to(window, {
			duration: 1.2,
			scrollTo: '#landing-sec',
			ease: 'power1.inOut'
		});
	};

	const scrollToDept = () => {
		gsap.to(window, {
			duration: 1.2,
			scrollTo: '#dept-sec',
			ease: 'power1.inOut'
		});
	};

	const scrollToTeam = () => {
		gsap.to(window, {
			duration: 1.2,
			scrollTo: '#team-sec',
			ease: 'power1.inOut'
		});
	};

	const scrollToContact = () => {
		gsap.to(window, {
			duration: 1.2,
			scrollTo: '#footer-sec',
			ease: 'power1.inOut'
		});
	};
</script>

<aside
	onmouseenter={() => (navrailOpen = true)}
	onmouseleave={() => (navrailOpen = false)}
	class="absolute z-20 flex {navrailOpen
		? 'translate-x-[0%]'
		: 'translate-x-[-100%]'} max-h-screen min-h-screen bg-[#3A6351]/80 p-8 transition-[translate] duration-200 ease-in-out"
>
	<div class="flex h-full flex-col items-center justify-center gap-3">
		<button
			onclick={scrollToHome}
			class="btn btn-lg font-kanit w-36 min-w-fit cursor-pointer rounded-full font-light shadow-none hover:border-[#3A6351] hover:bg-[#3A6351] hover:text-white"
			>Home</button
		>
		<button
			onclick={scrollToDept}
			class="btn btn-lg font-kanit w-36 min-w-fit cursor-pointer rounded-full font-light shadow-none hover:border-[#3A6351] hover:bg-[#3A6351] hover:text-white"
			>Departments</button
		>
		<button
			onclick={scrollToTeam}
			class="btn btn-lg font-kanit w-36 min-w-fit cursor-pointer rounded-full font-light shadow-none hover:border-[#3A6351] hover:bg-[#3A6351] hover:text-white"
			>Team</button
		>
		<button
			onclick={scrollToContact}
			class="btn btn-lg font-kanit w-36 min-w-fit cursor-pointer rounded-full font-light shadow-none hover:border-[#3A6351] hover:bg-[#3A6351] hover:text-white"
			>Contact</button
		>
	</div>
</aside>
