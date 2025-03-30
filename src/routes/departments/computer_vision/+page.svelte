<script lang="ts">
	import type { PageData } from './$types';
	// import { } from "../../../lib/images/dept_images/cv/thermal_imaging.png"

	let { data }: { data: PageData } = $props();
</script>

<input type="checkbox" id="cv-proj-2" class="modal-toggle" />
<div class="modal flex w-full flex-col items-center justify-center" role="dialog">
	<div class="modal-box flex h-[90%] !w-[60%] !max-w-full flex-col gap-y-7">
		<h3 class="font-kanit text-center text-4xl font-bold">
			Objection Detection using Thermal Imaging Camera
		</h3>
		<div class="flex flex-col items-center justify-center gap-y-7">
			<img
				src="/src/lib/images/dept_images/cv/thermal_imaging.png"
				class="h-[26rem]"
				alt="thermal_imaging"
			/>
			<a
				href="https://www.tinkercad.com/things/4zaomXCqKvE/editel?sharecode=mJMEkcDn2BVW9ZeP65ccdaxq-RHERdvDQ2FF3fTezlk"
				target="_blank"
				class="btn hover:btn-primary p-5 text-2xl">Find out more about this simulation here</a
			>
		</div>
		<div class="modal-action">
			<label for="cv-proj-2" class="btn hover:btn-error">Close!</label>
		</div>
	</div>
</div>

<input type="checkbox" id="cv-proj-3" class="modal-toggle" />
<div class="modal flex w-full flex-col items-center justify-center" role="dialog">
	<div class="modal-box flex h-[90%] !w-[60%] !max-w-full flex-col gap-y-7">
		<h3 class="font-kanit text-center text-4xl font-bold">Gesture controlled device switch</h3>
		<div class="flex flex-col items-center justify-center gap-y-7">
			<img
				src="/src/lib/images/dept_images/cv/cv-proj-3.png"
				class="h-[26rem]"
				alt="thermal_imaging"
			/>
			<a
				href="https://www.tinkercad.com/things/id9DlXaa2Zo-gesture-control-simulation/editel?returnTo=https%3A%2F%2Fwww.tinkercad.com%2Fdashboard&sharecode=0JXSgxLohKDK9rw4TkHF2HQ5sljCF3oLptvVVn0EPuU"
				target="_blank"
				class="btn hover:btn-primary p-5 text-2xl">Find out more about this simulation here</a
			>
		</div>
		<div class="modal-action">
			<label for="cv-proj-3" class="btn hover:btn-error">Close!</label>
		</div>
	</div>
</div>

<input type="checkbox" id="cv-proj-4" class="modal-toggle" />
<div class="modal flex w-full flex-col items-center justify-center" role="dialog">
	<div class="modal-box flex h-[90%] !w-[60%] !max-w-full flex-col gap-y-7">
		<h3 class="font-kanit text-center text-4xl font-bold">Face Detection based door lock</h3>
		<div class="flex flex-col items-center justify-center gap-y-7">
			<img
				src="/src/lib/images/dept_images/cv/cv-proj-4.png"
				class="h-[26rem]"
				alt="thermal_imaging"
			/>
			<a
				href="https://www.tinkercad.com/things/gU26ZlUNKoE-powerful-leelo-gaaris?sharecode=lY8w-XzHrQkRxMLgXN1QJEOO1JFryehTrLEa-6vnPnk"
				target="_blank"
				class="btn hover:btn-primary p-5 text-2xl">Find out more about this simulation here</a
			>
		</div>
		<div class="modal-action">
			<label for="cv-proj-4" class="btn hover:btn-error">Close!</label>
		</div>
	</div>
</div>

<main
	class="dotted-background-wrapper !bg-cv-primary flex min-h-screen flex-col items-center justify-center text-white"
>
	<div class="flex h-full w-full flex-col">
		<div class="flex h-[20%] flex-col items-center justify-center pt-28 pb-12">
			<h1
				class="cv-card-title font-bebas text-9xl text-white"
				style:--cv-title-text="cv-title-text"
			>
				Computer Vision
			</h1>
		</div>

		<div class="flex flex-col items-center">
			<div class="flex flex-col items-center gap-y-2">
				<h2 class="font-pixelify text-3xl font-bold">Project Head</h2>
				<div class="avatar">
					<div class="ring-offset-cv-primary w-24 rounded-full ring-4 ring-white ring-offset-2">
						<img
							src="https://img.daisyui.com/images/stock/photo-1534528741775-53994a69daeb.webp"
							alt="cv_dept_head"
						/>
					</div>
				</div>
				<p class="font-inria-sans text-2xl font-bold">Mahaswetha S</p>
			</div>
		</div>

		<div class="flex h-screen flex-col gap-y-2">
			<h1 class="font-bebas pt-12 pb-0 pl-12 text-6xl">Our Projects</h1>
			<div class="flex w-full grow flex-row items-center justify-center gap-x-4 p-4">
				<div class="card bg-cv-accent h-[60%] w-[40%]">
					<div class="card-body">
						<h2 class="card-title text-3xl">Obstacle avoidance robot</h2>
						<p>
							A card component has a figure, a body part, and inside body there are title and
							actions parts
						</p>
						<div class="card-actions justify-end">
							<!-- <label for="cv-proj-2" class="btn bg-cv-primary border-none shadow-none text-white"
								>Read More</label
							> -->
						</div>
					</div>
				</div>

				<div class="card bg-cv-accent h-[60%] w-[40%]">
					<div class="card-body">
						<h2 class="card-title text-3xl">Objection Detection using Thermal Imaging Camera</h2>
						<p>
							A card component has a figure, a body part, and inside body there are title and
							actions parts
						</p>
						<div class="card-actions justify-end">
							<label for="cv-proj-2" class="btn bg-cv-primary border-none text-white shadow-none"
								>Read More</label
							>
						</div>
					</div>
				</div>

				<div class="card bg-cv-accent h-[60%] w-[40%]">
					<div class="card-body">
						<h2 class="card-title text-3xl">Gesture controlled device switch</h2>
						<p>
							A card component has a figure, a body part, and inside body there are title and
							actions parts
						</p>
						<div class="card-actions justify-end">
							<label for="cv-proj-3" class="btn bg-cv-primary border-none text-white shadow-none"
								>Read More</label
							>
						</div>
					</div>
				</div>

				<div class="card bg-cv-accent h-[60%] w-[40%]">
					<div class="card-body">
						<h2 class="card-title text-3xl">Face Detection based door lock</h2>
						<p>
							A card component has a figure, a body part, and inside body there are title and
							actions parts
						</p>
						<div class="card-actions justify-end">
							<label for="cv-proj-4" class="btn bg-cv-primary border-none text-white shadow-none"
								>Read More</label
							>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</main>

<style>
	.dotted-background-wrapper {
		background-color: transparent;
		background: radial-gradient(circle, white 10%, transparent 1%) 0 0 / 20px 20px;
		background-size: 35px 35px;
		animation: moveLeft 2s linear infinite;
	}

	@keyframes moveLeft {
		0% {
			background-position: 0 0;
		}
		100% {
			background-position: 35px -35px;
		}
	}

	.cv-card-title {
		view-transition-name: var(--cv-title-text);
	}
</style>
