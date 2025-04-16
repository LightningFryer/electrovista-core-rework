<script lang="ts">
	import { onMount } from 'svelte';
	import gsap from 'gsap';
	import { ScrollTrigger } from 'gsap/ScrollTrigger';
	import { blobStoreUrl } from '$lib/blobStoreUrl';
	onMount(() => {
		gsap.registerPlugin(ScrollTrigger);
		gsap.from('.meet-the-team-card-elements', {
			duration: 0.6,
			opacity: 0,
			yPercent: 100,
			stagger: 0.2,
			paused: true,
			scrollTrigger: {
				trigger: '.meet-the-team-text-trigger',
				// markers: true,
				start: 'top 60%'
			}
		});
	});
</script>

<main
	class="dotted-background-wrapper flex min-h-screen flex-col items-center justify-center !bg-[#171717]"
	id="team-sec"
>
	<div class="meet-the-team-text-trigger flex min-h-[100vh] w-[90%] flex-col gap-y-10 text-center">
		<h1 class="meet-the-team-card-elements font-league-gothic text-7xl text-white md:text-9xl">
			MEET OUR TEAM
		</h1>
		<h2 class="meet-the-team-card-elements font-league-gothic text-5xl text-white md:text-6xl">
			Faculty Advisors
		</h2>
		<div
			class="flex flex-col items-center justify-center gap-y-12 md:flex-row md:gap-x-5 md:gap-y-0"
		>
			<div
				class="card meet-the-team-card-elements flex flex-col items-center justify-center bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem] md:h-[30rem] md:w-[40rem]"
			>
				<figure class="px-10 pt-10">
					<div class="avatar">
						<div class="w-48 rounded-full">
							<img src={`${blobStoreUrl}/images/team/shwetha_faculty.png`} alt="" />
						</div>
					</div>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-3xl md:text-5xl">Dr. Shwetha M</h2>
					<p class="font-inria-sans text-lg md:text-2xl">
						Assistant Professor – Senior Scale Department of Electronics & Communications
					</p>
					<!-- <div class="card-actions">
						<button class="btn">Know more</button>
					</div> -->
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements flex flex-col items-center justify-center bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem] md:h-[30rem] md:w-[40rem]"
			>
				<figure class="px-10 pt-10">
					<div class="avatar">
						<div class="w-48 rounded-full">
							<img src={`${blobStoreUrl}/images/team/soumya_faculty.png`} alt="" />
						</div>
					</div>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-3xl md:text-4xl">Dr. Soumya Sundar Pattanayak</h2>
					<p class="font-inria-sans text-lg md:text-2xl">
						Assistant Professor Department of Electronics & Communications
					</p>
					<!-- <div class="card-actions">
						<button class="btn">Know more</button>
					</div> -->
				</div>
			</div>
		</div>
		<h2 class="meet-the-team-card-elements font-league-gothic text-5xl text-white md:text-6xl">
			Core Committee
		</h2>

		<div
			class="grid grow grid-cols-1 place-items-center gap-y-6 p-6 md:grid-cols-5 md:gap-x-6 md:gap-y-4"
		>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<div class="avatar">
						<div class="w-32 rounded-full">
							<img src={`${blobStoreUrl}/images/team/tarunika.png`} alt="" />
						</div>
					</div>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-3xl">Tarunika</h2>
					<p class="font-inria-sans text-xl">President</p>
					<!-- <div class="card-actions">
						<button class="btn">Know more</button>
					</div> -->
				</div>
			</div>

			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<div class="avatar">
						<div class="w-32 rounded-full">
							<img src={`${blobStoreUrl}/images/team/jathin.png`} alt="" />
						</div>
					</div>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-xl">Jathin Bharadwaz P</h2>
					<p class="font-inria-sans text-xl">Vice president</p>
					<!-- <div class="card-actions">
						<button class="btn">Know more</button>
					</div> -->
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<div class="avatar">
						<div class="w-32 rounded-full">
							<img src={`${blobStoreUrl}/images/team/rishiraj.png`} alt="" />
						</div>
					</div>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-3xl">Rishiraj</h2>
					<p class="font-inria-sans text-xl">General secretary</p>
					<!-- <div class="card-actions">
						<button class="btn">Know more</button>
					</div> -->
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<div class="avatar">
						<div class="w-32 rounded-full">
							<img src={`${blobStoreUrl}/images/team/bhoomi.png`} alt="" />
						</div>
					</div>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-3xl">Bhoomi Varma</h2>
					<p class="font-inria-sans text-xl">Joint secretary</p>
					<!-- <div class="card-actions">
						<button class="btn">Know more</button>
					</div> -->
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<div class="avatar">
						<div class="w-32 rounded-full">
							<img src={`${blobStoreUrl}/images/team/swaminath.png`} alt="" />
						</div>
					</div>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-3xl">Swaminath</h2>
					<p class="font-inria-sans text-xl">Treasurer</p>
					<!-- <div class="card-actions">
						<button class="btn">Know more</button>
					</div> -->
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<div class="avatar">
						<div class="w-32 rounded-full">
							<img src={`${blobStoreUrl}/images/team/sreelakshmi.png`} alt="" />
						</div>
					</div>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-3xl">Sree lakshmi</h2>
					<p class="font-inria-sans text-xl">Logistics</p>
					<!-- <div class="card-actions">
						<button class="btn">Know more</button>
					</div> -->
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<div class="avatar">
						<div class="w-32 rounded-full">
							<img src={`${blobStoreUrl}/images/team/justin.png`} alt="" />
						</div>
					</div>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-3xl">Justin</h2>
					<p class="font-inria-sans text-xl">PR Head</p>
					<!-- <div class="card-actions">
						<button class="btn">Know more</button>
					</div> -->
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<div class="avatar">
						<div class="w-32 rounded-full">
							<img src={`${blobStoreUrl}/images/team/priyam.png`} alt="" />
						</div>
					</div>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-3xl">Priyam</h2>
					<p class="font-inria-sans text-xl">PR joint head</p>
					<!-- <div class="card-actions">
						<button class="btn">Know more</button>
					</div> -->
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<div class="avatar">
						<div class="w-32 rounded-full">
							<img src={`${blobStoreUrl}/images/team/vaisakh.png`} alt="" />
						</div>
					</div>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-2xl">Vaisakh Melaveetil</h2>
					<p class="font-inria-sans text-xl">Graphic Designer Head</p>
					<!-- <div class="card-actions">
						<button class="btn">Know more</button>
					</div> -->
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<div class="avatar">
						<div class="w-32 rounded-full">
							<img
								src={`https://v1a3dpktdo3ogcjf.public.blob.vercel-storage.com/images/team_card_images/mahadev_team_card.avif`}
								alt=""
							/>
						</div>
					</div>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-3xl">Mahadev</h2>
					<p class="font-inria-sans text-xl">Webmaster</p>
					<!-- <div class="card-actions">
						<button class="btn">Know more</button>
					</div> -->
				</div>
			</div>
		</div>
	</div>

	<h2 class="meet-the-team-card-elements font-league-gothic p-4 text-5xl text-white md:text-6xl">
		Domain Heads
	</h2>

	<div
		class="col-auto grid grow grid-cols-1 items-center justify-center gap-y-6 p-6 md:grid-cols-4 md:gap-x-6 md:gap-y-4"
	>
		<div
			class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
		>
			<figure class="px-10 pt-10">
				<div class="avatar">
					<div class="w-32 rounded-full">
						<img src={`${blobStoreUrl}/images/team/mahaswetha.png`} alt="" />
					</div>
				</div>
			</figure>
			<div class="card-body items-center text-center">
				<h2 class="card-title font-kanit text-3xl">Mahaswetha S</h2>
				<p class="font-inria-sans text-xl">Head of Computer Vision</p>
				<!-- <div class="card-actions">
						<button class="btn">Know more</button>
					</div> -->
			</div>
		</div>

		<div
			class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
		>
			<figure class="px-10 pt-10">
				<div class="avatar">
					<div class="w-32 rounded-full">
						<img src={`${blobStoreUrl}/images/team/sumukh.png`} alt="" />
					</div>
				</div>
			</figure>
			<div class="card-body items-center text-center">
				<h2 class="card-title font-kanit text-3xl">CKD Sumukh</h2>
				<p class="font-inria-sans text-xl">Head of Robotronics</p>
				<!-- <div class="card-actions">
						<button class="btn">Know more</button>
					</div> -->
			</div>
		</div>

		<div
			class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
		>
			<figure class="px-10 pt-10">
				<div class="avatar">
					<div class="w-32 rounded-full">
						<img src={`${blobStoreUrl}/images/team/sumedh.png`} alt="" />
					</div>
				</div>
			</figure>
			<div class="card-body items-center text-center">
				<h2 class="card-title font-kanit text-xl">Sumedh Prabhudesai</h2>
				<p class="font-inria-sans text-lg">Head of Embedded Systems</p>
				<!-- <div class="card-actions">
						<button class="btn">Know more</button>
					</div> -->
			</div>
		</div>

		<div
			class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
		>
			<figure class="px-10 pt-10">
				<div class="avatar">
					<div class="w-32 rounded-full">
						<img src={`${blobStoreUrl}/images/team/dheeraj.png`} alt="" />
					</div>
				</div>
			</figure>
			<div class="card-body items-center text-center">
				<h2 class="card-title font-kanit text-2xl">Dheeraj Anandan</h2>
				<p class="font-inria-sans text-lg">Head of IOT and Circuitry</p>
				<!-- <div class="card-actions">
						<button class="btn">Know more</button>
					</div> -->
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
</style>
