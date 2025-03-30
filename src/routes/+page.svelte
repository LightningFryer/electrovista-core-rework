<script>
	import Navbar from '$lib/components/Navbar.svelte';
	import Navrail from '$lib/components/Navrail.svelte';
	import Splash from '$lib/components/Splash.svelte';
	import Departments from '$lib/sections/Departments.svelte';
	import Landing from '$lib/sections/Landing.svelte';

	import gsap from 'gsap';
	import { onMount } from 'svelte';

	onMount(() => {
		gsap
			.fromTo(
				'.pop-text-1',
				{
					opacity: 0,
					display: 'none',
					scale: 5
				},
				{
					duration: 1,
					opacity: 1,
					scale: 1,
					display: 'block',
					ease: 'power4.inOut',
					onComplete: () => {
						gsap.set('.pop-text-1', {
							display: 'none'
						});
					}
				}
			)
			.then(() => {
				gsap
					.fromTo(
						'.pop-text-2',
						{
							opacity: 0,
							display: 'none',
							scale: 5
						},
						{
							duration: 1,
							opacity: 1,
							scale: 1,
							display: 'block',
							ease: 'power4.inOut',
							onComplete: () => {
								gsap.set('.pop-text-2', {
									display: 'none'
								});
							}
						}
					)
					.then(() => {
						gsap.fromTo(
							'.pop-text-3',
							{
								opacity: 0,
								display: 'none',
								scale: 5
							},
							{
								duration: 1,
								opacity: 1,
								scale: 1,
								display: 'block',
								ease: 'power4.inOut',
								onComplete: () => {
									gsap.set('.pop-text-3', {
										display: 'none',
										onComplete: () => {
											gsap.to('.splash-container', {
												duration: 1,
												yPercent: -100,
												ease: 'power3.inOut'
											});
										}
									});
								}
							}
						);
					});
			});
	});
</script>

<main class="min-h-screen overflow-x-hidden">
	<!-- <Splash /> -->
	<Navbar />
	<Navrail />
	<Landing />
    <Departments />
</main>
