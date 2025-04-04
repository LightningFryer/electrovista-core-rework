<script lang="ts">
	import { onMount } from 'svelte';
	import gsap from 'gsap';
	import { ScrollTrigger } from 'gsap/ScrollTrigger';
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
>
	<div class="meet-the-team-text-trigger flex min-h-[100vh] w-[90%] flex-col text-center">
		<h1 class="meet-the-team-card-elements font-league-gothic text-7xl text-white md:text-9xl">
			MEET OUR <span class="text-yellow-300">ELECTRIC</span> TEAM
		</h1>
		<div class="grid grow grid-cols-1 gap-y-6 p-6 md:grid-cols-5 md:gap-x-6 md:gap-y-4">
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<img
						src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp"
						alt="Shoes"
						class="rounded-xl"
					/>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-2xl">NAME</h2>
					<p class="font-inria-sans">Designation</p>
					<div class="card-actions">
						<button class="btn">Know more</button>
					</div>
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<img
						src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp"
						alt="Shoes"
						class="rounded-xl"
					/>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-2xl">NAME</h2>
					<p class="font-inria-sans">Designation</p>
					<div class="card-actions">
						<button class="btn">Know more</button>
					</div>
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<img
						src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp"
						alt="Shoes"
						class="rounded-xl"
					/>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-2xl">NAME</h2>
					<p class="font-inria-sans">Designation</p>
					<div class="card-actions">
						<button class="btn">Know more</button>
					</div>
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<img
						src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp"
						alt="Shoes"
						class="rounded-xl"
					/>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-2xl">NAME</h2>
					<p class="font-inria-sans">Designation</p>
					<div class="card-actions">
						<button class="btn">Know more</button>
					</div>
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<img
						src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp"
						alt="Shoes"
						class="rounded-xl"
					/>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-2xl">NAME</h2>
					<p class="font-inria-sans">Designation</p>
					<div class="card-actions">
						<button class="btn">Know more</button>
					</div>
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<img
						src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp"
						alt="Shoes"
						class="rounded-xl"
					/>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-2xl">NAME</h2>
					<p class="font-inria-sans">Designation</p>
					<div class="card-actions">
						<button class="btn">Know more</button>
					</div>
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<img
						src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp"
						alt="Shoes"
						class="rounded-xl"
					/>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-2xl">NAME</h2>
					<p class="font-inria-sans">Designation</p>
					<div class="card-actions">
						<button class="btn">Know more</button>
					</div>
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<img
						src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp"
						alt="Shoes"
						class="rounded-xl"
					/>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-2xl">NAME</h2>
					<p class="font-inria-sans">Designation</p>
					<div class="card-actions">
						<button class="btn">Know more</button>
					</div>
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<img
						src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp"
						alt="Shoes"
						class="rounded-xl"
					/>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-2xl">NAME</h2>
					<p class="font-inria-sans">Designation</p>
					<div class="card-actions">
						<button class="btn">Know more</button>
					</div>
				</div>
			</div>
			<div
				class="card meet-the-team-card-elements h-[20rem] w-[16rem] bg-[#3A6351]/50 text-white shadow-sm backdrop-blur-[0.1rem]"
			>
				<figure class="px-10 pt-10">
					<img
						src="https://img.daisyui.com/images/stock/photo-1606107557195-0e29a4b5b4aa.webp"
						alt="Shoes"
						class="rounded-xl"
					/>
				</figure>
				<div class="card-body items-center text-center">
					<h2 class="card-title font-kanit text-2xl">NAME</h2>
					<p class="font-inria-sans">Designation</p>
					<div class="card-actions">
						<button class="btn">Know more</button>
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
</style>
