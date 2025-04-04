<script>
	import Footer from '$lib/components/Footer.svelte';
	import Navbar from '$lib/components/Navbar.svelte';
	import Navrail from '$lib/components/Navrail.svelte';
	import Splash from '$lib/components/Splash.svelte';
	import Departments from '$lib/sections/Departments.svelte';
	import Landing from '$lib/sections/Landing.svelte';
	import MeetTheTeam from '$lib/sections/MeetTheTeam.svelte';

	import gsap from 'gsap';
	import { ScrollTrigger } from 'gsap/ScrollTrigger';
	import { onMount } from 'svelte';

	onMount(() => {
		if (sessionStorage.getItem('animationPlayed')) {
			gsap.set('.splash-container', { yPercent: -100 });
			return;
		}

		// Disable scrolling when splash is playing
		document.body.style.overflow = 'hidden';

		gsap
			.fromTo(
				'.pop-text-1',
				{ opacity: 0, display: 'none', scale: 5 },
				{
					duration: 1,
					opacity: 1,
					scale: 1,
					display: 'block',
					ease: 'power4.inOut',
					onComplete: () => {
						gsap.set('.pop-text-1', { display: 'none' });
					}
				}
			)
			.then(() => {
				return gsap.fromTo(
					'.pop-text-2',
					{ opacity: 0, display: 'none', scale: 5 },
					{
						duration: 1,
						opacity: 1,
						scale: 1,
						display: 'block',
						ease: 'power4.inOut',
						onComplete: () => {
							gsap.set('.pop-text-2', { display: 'none' });
						}
					}
				);
			})
			.then(() => {
				return gsap.fromTo(
					'.pop-text-3',
					{ opacity: 0, display: 'none', scale: 5 },
					{
						duration: 1,
						opacity: 1,
						scale: 1,
						display: 'block',
						ease: 'power4.inOut',
						onComplete: () => {
							gsap.set('.pop-text-3', { display: 'none' });
							gsap.to('.splash-container', {
								duration: 1,
								yPercent: -100,
								ease: 'power3.inOut',
								onComplete: () => {
									// Re-enable scrolling after animation ends
									document.body.style.overflow = '';
								}
							});
						}
					}
				);
			})
			.then(() => {
				sessionStorage.setItem('animationPlayed', 'true');
			});
	});
</script>

<svelte:head>
	<title>Electrovista | Home</title>
</svelte:head>

<main class="min-h-screen overflow-hidden">
	<Splash />
	<Navbar />
	<Navrail />
	<Landing />
	<Departments />
	<MeetTheTeam />
	<Footer />
</main>
