<script>
	import { blobStoreUrl } from '$lib/blobStoreUrl';
	import { onMount } from 'svelte';

	import gsap from 'gsap';
	import { ScrollTrigger } from 'gsap/ScrollTrigger';
	onMount(() => {
		gsap.registerPlugin(ScrollTrigger);
		gsap.from('.dept-card-elements', {
			duration: 0.6,
			opacity: 0,
			yPercent: 100,
			stagger: 0.2,
			paused: true,
			scrollTrigger: {
				trigger: '.dept-welcome-text-trigger',
				// markers: true,
				start: 'top 60%'
			}
		});
	});
</script>

<main
	class="dotted-background-wrapper flex min-h-screen flex-col items-center justify-center !bg-[#171717]"
>
	<div class="flex h-[90%] w-[95%] flex-col">
		<div class="dept-welcome-text-trigger mt-16 mb-12">
			<h1
				id="dept-welcome-text"
				class="dept-card-elements font-bebas text-center text-7xl text-white"
			>
				Check out our
			</h1>
			<h1
				id="dept-welcome-text"
				class="dept-card-elements font-bebas text-center text-7xl text-white"
			>
				Departments
			</h1>
		</div>

		<div
			class="flex grow flex-col items-center justify-center gap-y-10 pb-12 md:flex-row md:gap-x-6 md:pb-0"
		>
			<div class="card dept-card-elements bg-es-primary h-84 w-80 text-white">
				<figure class="px-6 pt-6">
					<img
						src={`${blobStoreUrl}/images/logos/club_logo_es.png`}
						alt="Shoes"
						class="h-16 rounded-xl bg-white"
					/>
				</figure>
				<div class="card-body items-center text-center">
					<h2
						class="es-card-title card-title font-bebas text-4xl tracking-wider md:text-2xl"
						style:--es-title-text="es-title-text"
					>
						Embedded Systems
					</h2>
					<p>
						A card component has a figure, a body part, and inside body there are title and actions
						parts
					</p>
					<div class="card-actions">
						<a
							href="departments/embedded_systems"
							class="btn border-none bg-[#edd183] text-white shadow-none">Visit Projects</a
						>
					</div>
				</div>
			</div>

			<div class="card dept-card-elements h-84 w-80 bg-[#38b6ff] text-white">
				<figure class="px-6 pt-6">
					<img
						src={`${blobStoreUrl}/images/logos/club_logo_iot.png`}
						alt="Shoes"
						class="h-16 rounded-xl bg-white"
					/>
				</figure>
				<div class="card-body items-center text-center">
					<h2
						class="iot-card-title card-title font-bebas text-4xl tracking-wider md:text-2xl"
						style:--iot-title-text="iot-title-text"
					>
						Internet of Things
					</h2>
					<p>
						A card component has a figure, a body part, and inside body there are title and actions
						parts
					</p>
					<div class="card-actions">
						<a href="departments/iot" class="btn border-none bg-[#253d95] text-white shadow-none"
							>Visit Projects</a
						>
					</div>
				</div>
			</div>

			<div class="card dept-card-elements h-84 w-80 bg-[#4f2882] text-white">
				<figure class="px-6 pt-6">
					<img
						src={`${blobStoreUrl}/images/logos/club_logo_cv.png`}
						alt="Shoes"
						class="h-16 rounded-xl bg-white"
					/>
				</figure>
				<div class="card-body items-center text-center">
					<h2
						class="cv-card-title card-title font-bebas text-4xl tracking-wider md:text-2xl"
						style:--cv-title-text="cv-title-text"
					>
						Computer Vision
					</h2>
					<p>
						A card component has a figure, a body part, and inside body there are title and actions
						parts
					</p>
					<div class="card-actions">
						<a
							href="/departments/computer_vision"
							class="btn border-none bg-[#ad7ded] text-white shadow-none">Visit Projects</a
						>
					</div>
				</div>
			</div>

			<div class="card dept-card-elements bg-circuitry-primary h-84 w-80 text-white">
				<figure class="px-6 pt-6">
					<img
						src={`${blobStoreUrl}/images/logos/club_logo_circuitry.png`}
						alt="Shoes"
						class="h-16 rounded-xl bg-white"
					/>
				</figure>
				<div class="card-body items-center text-center">
					<h2
						class="circuitry-card-title card-title font-bebas text-4xl tracking-wider md:text-2xl"
						style:--circuitry-title-text="circuitry-title-text"
					>
						Circuitry
					</h2>
					<p>
						A card component has a figure, a body part, and inside body there are title and actions
						parts
					</p>
					<div class="card-actions">
						<a
							href="departments/circuitry"
							class="btn bg-circuitry-accent border-none text-white shadow-none">Visit Projects</a
						>
					</div>
				</div>
			</div>

			<div class="card dept-card-elements h-84 w-80 bg-[#737373] text-white">
				<figure class="px-6 pt-6">
					<img
						src={`${blobStoreUrl}/images/logos/club_logo_robo.png`}
						alt="Shoes"
						class="h-16 rounded-xl bg-white"
					/>
				</figure>
				<div class="card-body items-center text-center">
					<h2
						class="robo-card-title card-title font-bebas text-4xl tracking-wider md:text-2xl"
						style:--robo-title-text="robo-title-text"
					>
						Robotronics
					</h2>
					<p>
						A card component has a figure, a body part, and inside body there are title and actions
						parts
					</p>
					<div class="card-actions">
						<a
							href="departments/robotronics"
							class="btn border-none bg-[#d4d4d4] text-white shadow-none">Visit Projects</a
						>
					</div>
				</div>
			</div>
		</div>
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

	.es-card-title {
		view-transition-name: var(--es-title-text);
	}

	.iot-card-title {
		view-transition-name: var(--iot-title-text);
	}

	.cv-card-title {
		view-transition-name: var(--cv-title-text);
	}

	.circuitry-card-title {
		view-transition-name: var(--circuitry-title-text);
	}

	.robo-card-title {
		view-transition-name: var(--robo-title-text);
	}
</style>
