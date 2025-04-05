<script lang="ts">
	import { blobStoreUrl } from '$lib/blobStoreUrl';
	import type { PageData } from './$types';

	let { data }: { data: PageData } = $props();
</script>

<svelte:head>
	<title>Electrovista | Internet Of Things</title>
</svelte:head>

<input type="checkbox" id="robo-proj-1" class="modal-toggle" />
<div class="modal flex w-full flex-col items-center justify-center" role="dialog">
	<div class="modal-box flex h-[95%] !w-[95%] !max-w-full flex-col gap-y-7 md:!w-[60%]">
		<h3 class="font-kanit text-center text-2xl font-bold md:text-4xl">
			Bionic arm with flex sensors
		</h3>
		<div class="flex flex-col items-center justify-center gap-y-7">
			<figure>
				<video src={`${blobStoreUrl}/videos/robotronics/robo_proj_1_vid.mp4`} muted controls
				></video>
			</figure>
			<h3 class="font-kanit text-2xl font-semibold">Circuit Diagram</h3>
			<img src={`${blobStoreUrl}/images/dept_images/iot/iot-proj-1.jpg`} alt="" />
			<p class="font-inria-sans text-2xl">
				The ESP32-based Bionic Arm is a gesture-controlled robotic arm designed to mimic human hand
				movements using flex sensors and an MPU6050 IMU sensor. The system utilizes an ESP32
				microcontroller to process sensor data and control servo motors via a PCA9685 servo driver.
				Five flex sensors detect finger bending, while the MPU6050 tracks wrist orientation,
				enabling real-time movement of the robotic fingers and wrist. The ESP32 interprets these
				inputs and sends appropriate PWM signals to the servos, ensuring smooth and accurate motion
				replication.
			</p>
		</div>
		<div class="modal-action">
			<label for="robo-proj-1" class="btn hover:btn-error">Close!</label>
		</div>
	</div>
</div>

<main
	class="dotted-background-wrapper flex min-h-screen flex-col items-center justify-center !bg-[#38B6FF] text-white"
>
	<div class="flex h-full w-full flex-col">
		<div class="flex h-[20%] flex-col items-center justify-center pt-20 pb-12">
			<div
				style:--iot-title-text="iot-title-text"
				class="iot-card-title bg-iot-accent/85 flex w-full flex-row items-center justify-center p-4 text-white"
			>
				<h1 class="font-league-gothic text-4xl md:text-9xl">INTERNET</h1>
				<img
					src={`${blobStoreUrl}/images/logos/iot_base_logo.png`}
					class="max-h-20 rounded-full md:max-h-28"
					alt="es_logo_base"
				/>
				<h1 class="font-league-gothic text-4xl md:text-9xl">OF THINGS</h1>
			</div>
		</div>

		<div class="flex flex-col items-center">
			<div class="flex flex-col items-center gap-y-2">
				<h2 class="font-pixelify text-3xl font-bold">Project Head</h2>
				<div class="avatar">
					<div class="ring-offset-iot-primary w-36 rounded-full ring-4 ring-white ring-offset-2">
						<img src={`${blobStoreUrl}/images/team/dheeraj.png`} alt="iot_dept_head" />
					</div>
				</div>
				<p class="font-inria-sans text-3xl font-bold">Dheeraj Anandan</p>
			</div>
		</div>

		<div class="flex min-h-screen flex-col gap-y-2 md:h-screen">
			<h1 class="font-bebas pt-12 pb-0 text-center text-7xl md:text-8xl">Our Projects</h1>

			<div
				class="flex w-full grow flex-col items-center justify-center gap-x-4 gap-y-10 p-5 md:flex-row md:gap-y-0 md:p-6"
			>
				<div class="card bg-iot-accent md:h-[60%] md:w-[40%]">
					<div class="card-body">
						<h2 class="card-title font-kanit text-3xl">Bionic arm with flex sensors</h2>
						<p class="font-inria-sans text-lg">
							The ESP32-based Bionic Arm is a gesture-controlled robotic arm designed to mimic human
							hand movements using flex sensors and an MPU6050 IMU sensor.
						</p>
						<div class="card-actions justify-end">
							<label for="robo-proj-1" class="btn bg-iot-primary border-none shadow-none"
								>Read More</label
							>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
	<div class="flex w-full flex-col pr-12 pb-12 pl-12 md:-mt-12">
		<h1 class="font-bebas text-center text-2xl md:text-4xl">
			Thinking of a cool project? We’d love to hear from you—get in touch!
		</h1>
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

	.iot-card-title {
		view-transition-name: var(--iot-title-text);
	}
</style>
