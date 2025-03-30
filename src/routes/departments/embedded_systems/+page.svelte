<script lang="ts">
	import type { PageData } from './$types';

	let { data }: { data: PageData } = $props();
</script>

<input type="checkbox" id="my_modal_6" class="modal-toggle" />
<div class="modal" role="dialog">
	<div class="modal-box">
		<h3 class="text-lg font-bold">Hello!</h3>
		<p class="py-4">This modal works with a hidden checkbox!</p>
		<div class="modal-action">
			<label for="my_modal_6" class="btn">Close!</label>
		</div>
	</div>
</div>

<main
	class="dotted-background-wrapper text-purple flex min-h-screen flex-col items-center justify-center !bg-[#F1B81A]"
>
	<div class="flex h-full w-full flex-col">
		<div class="flex h-[20%] flex-col items-center justify-center pt-20 pb-12">
			<div
				style:--es-title-text="es-title-text"
				class="es-card-title bg-purple flex w-full flex-row items-center justify-center border-4 p-4"
			>
				<h1 class="text-es-accent font-league-gothic text-5xl md:text-9xl">EMBEDDED</h1>
				<img
					src="/src/lib/images/logos/es_base_logo.png"
					class="max-h-20 rounded-full md:max-h-32"
					alt="es_logo_base"
				/>
				<h1 class="text-es-accent font-league-gothic text-5xl md:text-9xl">SYSTEMS</h1>
			</div>
		</div>

		<div class="flex flex-col items-center">
			<div class="flex flex-col items-center gap-y-2">
				<h2 class="font-pixelify text-3xl font-bold">Project Head</h2>
				<div class="avatar">
					<div class="ring-purple ring-offset-es-primary w-24 rounded-full ring-4 ring-offset-2">
						<img
							src="https://img.daisyui.com/images/stock/photo-1534528741775-53994a69daeb.webp"
							alt="es_dept_head"
						/>
					</div>
				</div>
				<p class="font-inria-sans text-2xl font-bold">Sumedh Prabhudeshai</p>
			</div>
		</div>

		<div class="flex min-h-screen flex-col gap-y-2 md:h-screen">
			<h1 class="font-bebas pt-12 pb-0 pl-12 text-6xl">Our Projects</h1>

			<div
				class="flex w-full grow flex-col items-center justify-center gap-x-4 gap-y-10 p-5 md:flex-row md:gap-y-0 md:p-6"
			>
				<div class="card bg-es-accent md:h-[60%] md:w-[40%]">
					<div class="card-body">
						<h2 class="card-title text-3xl">
							Efficient Thermal Management System for Small Satellites
						</h2>
						<p>
							A card component has a figure, a body part, and inside body there are title and
							actions parts
						</p>
						<div class="card-actions justify-end">
							<!-- <button class="btn bg-es-primary border-none shadow-none">Read More!</button> -->
							<label for="my_modal_6" class="btn bg-es-primary border-none shadow-none"
								>Read More</label
							>
						</div>
					</div>
				</div>

				<div class="card bg-es-accent md:h-[60%] md:w-[40%]">
					<div class="card-body">
						<h2 class="card-title text-3xl">
							Hardware-Assisted Encryption for Resource-Constrained Devices
						</h2>
						<p>
							A card component has a figure, a body part, and inside body there are title and
							actions parts
						</p>
						<div class="card-actions justify-end">
							<button class="btn bg-es-primary border-none shadow-none">Read More!</button>
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
</style>
