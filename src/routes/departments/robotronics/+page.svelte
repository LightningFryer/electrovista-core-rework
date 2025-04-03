<script lang="ts">
	import type { PageData } from './$types';

	let { data }: { data: PageData } = $props();
</script>

<svelte:head>
	<title>Electrovista | Robotronics</title>
</svelte:head>

<input type="checkbox" id="robo_modal_1" class="modal-toggle" />
<div class="modal flex w-full flex-col items-center justify-center" role="dialog">
	<div class="modal-box flex h-[75%] !w-[60%] !max-w-full flex-col justify-between gap-y-7">
		<h3 class="font-kanit text-center text-4xl font-bold">Face Tracker robot</h3>
		<div class="font-inria-sans flex flex-col gap-y-5 text-2xl">
			<p>
				The Face Tracker, known as Beans, is a project that detects and follows human faces, adding
				a more interactive touch to AI-based systems. Unlike the other projects,it relies on OpenCV.
				The camera captures video input, a face detection algorithm finds a person’s face, and the
				system moves the servos accordingly to keep the face centered in view.
			</p>

			<p>
				This project makes AI seem more engaging and lifelike, perfect for interactive robotics,
				assistive devices, or fun tech demonstrations. Future improvements could include expression
				recognition, speech interaction, or even eye-tracking to enhance its responsiveness and make
				it feel more natural.
			</p>
		</div>
		<div class="modal-action">
			<label for="robo_modal_1" class="btn hover:btn-error">Close!</label>
		</div>
	</div>
</div>

<input type="checkbox" id="robo_modal_2" class="modal-toggle" />
<div class="modal flex w-full flex-col items-center justify-center" role="dialog">
	<div class="modal-box flex h-[75%] !w-[60%] !max-w-full flex-col justify-between gap-y-7">
		<h3 class="font-kanit text-center text-4xl font-bold">Solar Tracker robot</h3>
		<div class="font-inria-sans flex flex-col gap-y-5 text-2xl">
			<p>
				The Solar Tracker is an automated system designed to maximize the efficiency of solar panels
				by adjusting their position to follow the sun’s movement. It uses light-dependent resistors
				(LDRs) to detect the direction of maximum sunlight and an Arduino-controlled servo mechanism
				to reposition the panel accordingly. This dynamic tracking significantly improves energy
				absorption compared to fixed panels, making it an effective solution for small-scale
				renewable energy systems.
			</p>

			<p>
				The system continuously adjusts throughout the day, ensuring optimal alignment with the sun.
				To improve performance, additional features like dual-axis tracking can be implemented,
				allowing for even finer adjustments.
			</p>
		</div>
		<div class="modal-action">
			<label for="robo_modal_2" class="btn hover:btn-error">Close!</label>
		</div>
	</div>
</div>

<input type="checkbox" id="robo_modal_3" class="modal-toggle" />
<div class="modal flex w-full flex-col items-center justify-center" role="dialog">
	<div class="modal-box flex h-[75%] !w-[60%] !max-w-full flex-col justify-between gap-y-7">
		<h3 class="font-kanit text-center text-4xl font-bold">Light Tracker robot</h3>
		<div class="font-inria-sans flex flex-col gap-y-5 text-2xl">
			<p>
				The Light Tracker is designed to follow a moving light source using an Arduino, two LDRs,
				and a servo motor. It works by continuously comparing light levels detected by the LDRs and
				adjusting the servo to turn towards the brighter source. This simple yet effective mechanism
				enables the system to track a flashlight, laser pointer, or any other moving light.
			</p>

			<p>
				The system functions similarly to the solar tracker but is more responsive to rapid changes
				in light direction. It can be used in autonomous robots that navigate towards light,
				interactive installations, or smart lighting systems. By fine-tuning the sensor response and
				servo movement, the tracker can achieve smoother and faster reactions.
			</p>
		</div>
		<div class="modal-action">
			<label for="robo_modal_3" class="btn hover:btn-error">Close!</label>
		</div>
	</div>
</div>

<input type="checkbox" id="robo_modal_4" class="modal-toggle" />
<div class="modal flex w-full flex-col items-center justify-center" role="dialog">
	<div class="modal-box flex h-[75%] !w-[60%] !max-w-full flex-col justify-between gap-y-7">
		<h3 class="font-kanit text-center text-4xl font-bold">Self Balancing robot</h3>
		<div class="font-inria-sans flex flex-col gap-y-5 text-2xl">
			<p>
				The Self-Balancing System is a two-wheeled robot that stays upright using an Arduino, a
				gyroscope, and an accelerometer. These sensors detect any tilt, and the Arduino quickly
				adjusts the motors to counteract the motion, keeping the system balanced.
			</p>

			<p>
				The system uses PID control to ensure smooth and stable balancing, even when pushed or
				placed on uneven surfaces. Future improvements could include autonomous movement, obstacle
				avoidance, or machine learning-based stabilization to make it even more versatile.
			</p>
		</div>
		<div class="modal-action">
			<label for="robo_modal_4" class="btn hover:btn-error">Close!</label>
		</div>
	</div>
</div>

<main
	class="dotted-background-wrapper text-robotronics-accent !bg-robotronics-primary flex min-h-screen flex-col items-center justify-center"
>
	<div class="flex h-full w-full flex-col">
		<div class="flex h-[20%] flex-col items-center justify-center pt-28 pb-12">
			<div
				style:--circuitry-title-text="circuitry-title-text"
				class="circuitry-card-title bg-robotronics-accent/65 flex w-full flex-row items-center justify-center p-4 text-white"
			>
				<h1 class="font-league-gothic text-5xl md:text-9xl">ROBOT</h1>
				<img
					src="/src/lib/images/logos/robo_base_logo.png"
					class="max-h-20 rounded-full md:max-h-32"
					alt="es_logo_base"
				/>
				<h1 class="font-league-gothic text-5xl md:text-9xl">RONICS</h1>
			</div>
		</div>

		<div class="flex flex-col items-center">
			<div class="flex flex-col items-center gap-y-2">
				<h2 class="font-pixelify text-3xl font-bold">Project Head</h2>
				<div class="avatar">
					<div class="w-24 rounded-full ring-4 ring-[#737373] ring-offset-2 ring-offset-[#d4d4d4]">
						<img
							src="https://img.daisyui.com/images/stock/photo-1534528741775-53994a69daeb.webp"
							alt="robotronics_dept_head"
						/>
					</div>
				</div>
				<p class="font-inria-sans text-2xl font-bold">Sumedh Prabhudeshai</p>
			</div>
		</div>

		<div class="flex h-screen flex-col gap-y-2">
			<h1 class="font-bebas pt-12 pb-0 pl-12 text-6xl">Our Projects</h1>
			<div class="flex w-full grow flex-row items-center justify-center gap-x-4 p-6">
				<div class="card text-robotronics-primary h-[60%] w-[40%] bg-[#d4d4d4]">
					<div class="card-body">
						<h2 class="card-title text-3xl">Face Tracker robot</h2>
						<p class="">
							The Face Tracker, known as Beans, is a project that detects and follows human faces,
							adding a more interactive touch to AI-based systems. Unlike the other projects,it
							relies on OpenCV.
						</p>
						<div class="card-actions justify-end">
							<label for="robo_modal_1" class="btn border-none bg-[#737373] text-white shadow-none"
								>Read More</label
							>
						</div>
					</div>
				</div>

				<div class="card text-robotronics-primary h-[60%] w-[40%] bg-[#d4d4d4]">
					<div class="card-body">
						<h2 class="card-title text-3xl">Solar Tracker robot</h2>
						<p>
							The Solar Tracker is an automated system designed to maximize the efficiency of solar
							panels by adjusting their position to follow the sun’s movement.
						</p>
						<div class="card-actions justify-end">
							<label for="robo_modal_2" class="btn border-none bg-[#737373] text-white shadow-none"
								>Read More</label
							>
						</div>
					</div>
				</div>
				<div class="card text-robotronics-primary h-[60%] w-[40%] bg-[#d4d4d4]">
					<div class="card-body">
						<h2 class="card-title text-3xl">Light Tracker robot</h2>
						<p>
							The Light Tracker is designed to follow a moving light source using an Arduino, two
							LDRs, and a servo motor. It works by continuously comparing light levels detected by
							the LDRs and adjusting the servo to turn towards the brighter source.
						</p>
						<div class="card-actions justify-end">
							<label for="robo_modal_3" class="btn border-none bg-[#737373] text-white shadow-none"
								>Read More</label
							>
						</div>
					</div>
				</div>
				<div class="card text-robotronics-primary h-[60%] w-[40%] bg-[#d4d4d4]">
					<div class="card-body">
						<h2 class="card-title text-3xl">Self Balancing robot</h2>
						<p>
							The Self-Balancing System is a two-wheeled robot that stays upright using an Arduino,
							a gyroscope, and an accelerometer. These sensors detect any tilt, and the Arduino
							quickly adjusts the motors to counteract the motion, keeping the system balanced.
						</p>
						<div class="card-actions justify-end">
							<label for="robo_modal_4" class="btn border-none bg-[#737373] text-white shadow-none"
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

	.robotronics-card-title {
		view-transition-name: var(--robotronics-title-text);
	}
</style>
