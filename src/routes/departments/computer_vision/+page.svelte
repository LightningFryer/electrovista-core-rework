<script lang="ts">
	import { blobStoreUrl } from '$lib/blobStoreUrl';
	import type { PageData } from './$types';
	// import { } from "../../../lib/images/dept_images/cv/thermal_imaging.png"

	let { data }: { data: PageData } = $props();
</script>

<svelte:head>
	<title>Electrovista | Computer Vision</title>
</svelte:head>

<input type="checkbox" id="cv-proj-1" class="modal-toggle" />
<div class="modal flex w-full flex-col items-center justify-center" role="dialog">
	<div class="modal-box flex h-[95%] !w-[95%] !max-w-full flex-col gap-y-4 md:!w-[60%]">
		<h3 class="font-kanit text-center text-2xl font-bold md:text-4xl">Obstacle avoidance robot</h3>
		<div class="flex flex-col items-center justify-center gap-y-7">
			<figure>
				<video src={`${blobStoreUrl}/videos/cv/cv_proj_1_vid.mp4`} controls class="md:h-full"
				></video>
			</figure>
			<p class="font-inria-sans text-2xl">
				This is a robot that can detect and avoid obstacles in its path using ultrasonic sensors and
				camera vision.
			</p>

			<p class="font-kanit text-left text-4xl font-semibold">Features</p>
			<ul class="list-disc p-4">
				<li class="text-lg">
					<span class="font-semibold">Raspberry Pi Camera / USB Camera</span>: Captures real-time
					video for obstacle detection
				</li>
				<li class="text-lg">
					<span class="font-semibold">Raspberry Pi</span>: Processes video feed and applies Canny
					edge detection
				</li>
				<li class="text-lg">
					<span class="font-semibold">Motor Driver Module</span>: Controls motor movements based on
					detected obstacles
				</li>
				<li class="text-lg">
					<span class="font-semibold">DC Motors</span>: Enables the robot to navigate around
					obstacles
				</li>
			</ul>
			<p class="font-kanit text-left text-4xl font-semibold">How it Works</p>
			<ul class="list-disc p-6">
				<li class="text-lg">
					<span class="font-semibold">Canny Edge Detection</span>: Identifies obstacle edges in the
					video feed
				</li>
				<li class="text-lg">
					<span class="font-semibold">Region-Based Edge Analysis</span>:
					<ul class="list-disc pl-6">
						<li>More edges on the left? → Turn right</li>
						<li>More edges on the right? → Turn left</li>
						<li>Edges on both sides? → Stop</li>
						<li>No edges detected? → Move forward</li>
					</ul>
				</li>
				<li class="text-lg">
					<span class="font-semibold">Motor Control via Raspberry Pi GPIO</span>: Adjusts movement
					based on obstacle detection
				</li>
			</ul>
		</div>
		<div class="modal-action">
			<label for="cv-proj-1" class="btn hover:btn-error">Close!</label>
		</div>
	</div>
</div>

<input type="checkbox" id="cv-proj-2" class="modal-toggle" />
<div class="modal flex w-full flex-col items-center justify-center" role="dialog">
	<div class="modal-box flex h-[95%] !w-[95%] !max-w-full flex-col gap-y-4 md:!w-[60%]">
		<h3 class="font-kanit text-center text-2xl font-bold md:text-4xl">
			Objection Detection using Thermal Imaging Camera
		</h3>
		<div class="flex flex-col items-center justify-center gap-y-7">
			<img
				src="https://v1a3dpktdo3ogcjf.public.blob.vercel-storage.com/electrovista_core_images/images/dept_images/cv/cv-proj-2.png"
				class="md:h-[26rem]"
				alt="thermal_imaging"
			/>
			<a
				href="https://www.tinkercad.com/things/4zaomXCqKvE/editel?sharecode=mJMEkcDn2BVW9ZeP65ccdaxq-RHERdvDQ2FF3fTezlk"
				target="_blank"
				class="btn bg-[#3A6351] py-5 text-white hover:bg-[#3A6351]/90 md:text-2xl"
				>Find out more about this simulation here</a
			>
			<p class="font-kanit text-left text-2xl font-semibold">Components Comparison</p>
			<div class="">
				<table class="table">
					<thead class="">
						<tr class="text-xs">
							<th class="">Components</th>
							<th class="">Simulation model</th>
							<th class="">Real-world model</th>
						</tr>
					</thead>
					<tbody>
						<tr class="text-xs">
							<td class="">Microcontroller</td>
							<td class="">Arduino Uno3</td>
							<td class="">Raspberry Pi4</td>
						</tr>
						<tr class="text-xs">
							<td class="">Temperature sensor</td>
							<td class="">TMP36 (simulated)</td>
							<td class="">MLX90640 (thermal imaging sensor)</td>
						</tr>
						<tr class="text-xs">
							<td class="">Display</td>
							<td class="">16x2 LCD (non-I2C)</td>
							<td class="">Laptop display</td>
						</tr>
						<tr class="text-xs">
							<td class="">Cooling system</td>
							<td class="">Not required</td>
							<td class="">Heat sink and fan for Raspberry Pi</td>
						</tr>
						<tr class="text-xs">
							<td class="">Power supply</td>
							<td class="">Simulated 5V from Arduino</td>
							<td class="">5V USB-C adapter for Raspberry Pi</td>
						</tr>
					</tbody>
				</table>
			</div>

			<p class="font-kanit text-left text-2xl font-semibold">Simulation Components</p>
			<ul class="list-disc p-6">
				<li class="text-lg">
					<span class="font-semibold">Arduino Uno</span>: Acts as the microcontroller to process
					data and control the system
				</li>
				<li class="text-lg">
					<span class="font-semibold">TMP36 Temperature Sensor</span>: Simulates temperature
					readings and outputs an analog voltage
				</li>
				<li class="text-lg">
					<span class="font-semibold">16x2 LCD Display</span>: Displays the temperature and object
					classification
				</li>
				<li class="text-lg">
					<span class="font-semibold">Potentiometer</span>: Adjusts the contrast of the LCD display
				</li>
			</ul>

			<p class="font-kanit text-left text-2xl font-semibold">Simulation Flow</p>
			<ul class="list-disc p-6">
				<li class="text-lg">
					<span class="font-semibold">Temperature Sensing</span>:
					<ul class="list-disc pl-6">
						<li>TMP36 sensor simulates temperature readings</li>
						<li>Outputs an analog voltage proportional to the temperature</li>
						<li>Arduino reads the voltage and converts it into Celsius</li>
					</ul>
				</li>
				<li class="text-lg">
					<span class="font-semibold">Object Classification</span>:
					<ul class="list-disc pl-6">
						<li>Temperature above 30°C → Classified as Human/Dog</li>
						<li>Temperature below 30°C → Classified as Car/Bike</li>
					</ul>
				</li>
				<li class="text-lg">
					<span class="font-semibold">Display Output</span>:
					<ul class="list-disc pl-6">
						<li>First Line: Displays object classification (e.g., "Human/Dog" or "Car/Bike")</li>
						<li>Second Line: Displays temperature value in Celsius (e.g., "Temp: 35.00 C")</li>
					</ul>
				</li>
				<li class="text-lg">
					<span class="font-semibold">Adjusting Contrast</span>:
					<ul class="list-disc pl-6">
						<li>Potentiometer adjusts LCD contrast</li>
						<li>Turning the knob makes the text clearer or dimmer</li>
					</ul>
				</li>
			</ul>

			<p class="font-kanit text-left text-2xl font-semibold">Tinkercad Interaction</p>
			<ul class="list-disc p-6">
				<li class="text-lg">Manually adjust TMP36 temperature values</li>
				<li class="text-lg">Arduino processes new values and updates the LCD in real-time</li>
				<li class="text-lg">Observe object classification changes based on temperature</li>
			</ul>
		</div>
		<div class="modal-action">
			<label for="cv-proj-2" class="btn hover:btn-error">Close!</label>
		</div>
	</div>
</div>

<input type="checkbox" id="cv-proj-3" class="modal-toggle" />
<div class="modal flex w-full flex-col items-center justify-center" role="dialog">
	<div class="modal-box flex h-[95%] !w-[95%] !max-w-full flex-col gap-y-4 md:!w-[60%]">
		<h3 class="font-kanit text-center text-4xl font-bold">Gesture controlled device switch</h3>
		<div class="font-inria-sans flex flex-col items-center justify-center gap-y-7">
			<img
				src={`${blobStoreUrl}/images/dept_images/cv/cv-proj-3.png`}
				class="md:h-[26rem]"
				alt="thermal_imaging"
			/>
			<a
				href="https://www.tinkercad.com/things/id9DlXaa2Zo-gesture-control-simulation/editel?returnTo=https%3A%2F%2Fwww.tinkercad.com%2Fdashboard&sharecode=0JXSgxLohKDK9rw4TkHF2HQ5sljCF3oLptvVVn0EPuU"
				target="_blank"
				class="btn bg-[#3A6351] py-5 text-white hover:bg-[#3A6351]/90 md:text-2xl"
				>Find out more about this simulation here</a
			>
			<p class="text-lg">
				A user wants to control a bulb in their room using hand gestures. Instead of pressing a
				traditional switch, they can use a simple hand wave or other gestures to turn the bulb on or
				off. This makes it easier to control the appliance without physically interacting with a
				switch, which is especially useful for people with limited mobility or for anyone who wants
				a more modern way to interact with their home appliances.
			</p>

			<p class="font-kanit text-left text-2xl font-semibold">Raspberry Pi Setup</p>
			<ul class="list-disc p-6">
				<li class="text-lg">
					<span class="font-semibold">Raspberry Pi</span>: Any model with camera support (e.g.,
					Raspberry Pi 3 or 4)
				</li>
				<li class="text-lg">
					<span class="font-semibold">Relay Module</span>: Controls the table lamp based on detected
					gestures
				</li>
				<li class="text-lg">
					<span class="font-semibold">Camera Module</span>: Captures hand gestures for processing
					(via OpenCV or APDS-9960)
				</li>
				<li class="text-lg">
					<span class="font-semibold">LCD Screen (Optional)</span>: Displays lamp status and other
					information
				</li>
				<li class="text-lg">
					<span class="font-semibold">Power Supply</span>: Powers Raspberry Pi and connected
					components
				</li>
				<li class="text-lg">
					<span class="font-semibold">Wires & Connectors</span>: Connects the relay and other
					components
				</li>
				<li class="text-lg">
					<span class="font-semibold">Table Lamp</span>: Connected to the relay module for
					gesture-based control
				</li>
			</ul>

			<p class="font-kanit text-left text-2xl font-semibold">How It Works</p>
			<ul class="list-disc p-6">
				<li class="text-lg">
					<span class="font-semibold">Gesture Detection</span>:
					<ul class="list-disc pl-6">
						<li>Camera module captures real-time images of the user's hand</li>
						<li>OpenCV processes gestures like hand waves or specific hand shapes</li>
						<li>Example: Open hand → Turns light on, Fist → Turns light off</li>
					</ul>
				</li>
				<li class="text-lg">
					<span class="font-semibold">Control Logic</span>:
					<ul class="list-disc pl-6">
						<li>Raspberry Pi processes the camera feed to recognize gestures</li>
						<li>When a gesture is detected, Raspberry Pi triggers the relay module</li>
						<li>Relay is connected to GPIO pins, acting as a switch for the lamp</li>
						<li>Python script configures GPIO pins to send HIGH or LOW signals</li>
					</ul>
				</li>
				<li class="text-lg">
					<span class="font-semibold">Status Display</span>:
					<ul class="list-disc pl-6">
						<li>LCD screen (if connected) displays "On" or "Off" based on gesture recognition</li>
					</ul>
				</li>
				<li class="text-lg">
					<span class="font-semibold">Power Supply</span>:
					<ul class="list-disc pl-6">
						<li>Raspberry Pi requires a 5V power supply</li>
						<li>Relay module may need a separate power source depending on lamp voltage</li>
					</ul>
				</li>
			</ul>

			<p class="font-kanit text-left text-2xl font-semibold">
				Camera Setup and Gesture Recognition
			</p>
			<ul class="list-disc p-6">
				<li class="text-lg">
					Raspberry Pi camera module or external camera captures real-time images
				</li>
				<li class="text-lg">Python script in OpenCV processes camera feed and detects gestures</li>
				<li class="text-lg">Defines a region of interest (ROI) where hand detection occurs</li>
			</ul>

			<p class="font-kanit text-left text-2xl font-semibold">Relay Control via GPIO</p>
			<ul class="list-disc p-6">
				<li class="text-lg">GPIO pins control physical hardware based on gesture detection</li>
				<li class="text-lg">HIGH signal → Completes the relay circuit, turning lamp on</li>
				<li class="text-lg">LOW signal → Opens the circuit, turning lamp off</li>
			</ul>
		</div>
		<div class="modal-action">
			<label for="cv-proj-3" class="btn hover:btn-error">Close!</label>
		</div>
	</div>
</div>

<input type="checkbox" id="cv-proj-4" class="modal-toggle" />
<div class="modal flex w-full flex-col items-center justify-center" role="dialog">
	<div class="modal-box flex h-[95%] !w-[95%] !max-w-full flex-col gap-y-4 md:!w-[60%]">
		<h3 class="font-kanit text-center text-4xl font-bold">Face Detection based door lock</h3>
		<div class="flex flex-col items-center justify-center gap-y-7">
			<img
				src={`${blobStoreUrl}/images/dept_images/cv/cv-proj-4.png`}
				class="md:h-[26rem]"
				alt="thermal_imaging"
			/>
			<a
				href="https://www.tinkercad.com/things/gU26ZlUNKoE-powerful-leelo-gaaris?sharecode=lY8w-XzHrQkRxMLgXN1QJEOO1JFryehTrLEa-6vnPnk"
				target="_blank"
				class="btn bg-[#3A6351] py-5 text-white hover:bg-[#3A6351]/90 md:text-2xl"
				>Find out more about this simulation here</a
			>
			<p class="font-kanit text-left text-2xl font-semibold">Workflow</p>

			<ul class="list-disc p-6">
				<li class="text-lg">
					<span class="font-semibold">Face Detection and Recognition</span>:
					<ul class="list-disc pl-6">
						<li>Camera continuously captures frames for face detection</li>
						<li>Face detection algorithm processes the frames</li>
						<li>Detected face is compared against stored face data in the system</li>
					</ul>
				</li>
				<li class="text-lg">
					<span class="font-semibold">Triggering the Lock</span>:
					<ul class="list-disc pl-6">
						<li>Recognized face → Raspberry Pi sends signal to relay module</li>
						<li>Relay activates solenoid lock, unlocking the door</li>
						<li>Unrecognized face → System keeps door locked</li>
						<li>LCD screen displays "Access Denied" message</li>
					</ul>
				</li>
			</ul>

			<p class="font-kanit text-left text-2xl font-semibold">
				Steps for Face Database Implementation
			</p>

			<ul class="list-disc p-6">
				<li class="text-lg">
					<span class="font-semibold">Capture and Store Faces (Training Phase)</span>:
					<ul class="list-disc pl-6">
						<li>System captures and stores images of authorized users</li>
						<li>Images are saved in a database (folder labeled with each person's name)</li>
						<li>
							Once a face is added, the system trains the model (LBPH recognizer) for recognition
						</li>
					</ul>
				</li>
				<li class="text-lg">
					<span class="font-semibold">Training the Recognizer</span>:
					<ul class="list-disc pl-6">
						<li>Captured images are used to train the LBPH face recognizer</li>
						<li>The trained model is saved to a file for future face recognition</li>
					</ul>
				</li>
				<li class="text-lg">
					<span class="font-semibold">Face Recognition during Operation (Runtime Phase)</span>:
					<ul class="list-disc pl-6">
						<li>During normal operation, the camera detects faces in real-time</li>
						<li>Detected face is compared with stored data in the database</li>
						<li>Matched face → Unlocks door, Unmatched face → Access Denied</li>
					</ul>
				</li>
			</ul>
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
		<div class="flex h-[20%] flex-col items-center justify-center pt-20 pb-12">
			<div
				style:--cv-title-text="cv-title-text"
				class="cv-card-title flex w-full flex-row items-center justify-center bg-[#7E5CAD] p-4 text-white"
			>
				<h1 class="font-league-gothic text-5xl md:text-9xl">COMPUTER</h1>
				<img
					src={`${blobStoreUrl}/images/logos/cv_base_logo.png`}
					class="max-h-20 rounded-full md:max-h-32"
					alt="es_logo_base"
				/>
				<h1 class="font-league-gothic text-5xl md:text-9xl">VISION</h1>
			</div>
		</div>

		<div class="flex flex-col items-center">
			<div class="flex flex-col items-center gap-y-2">
				<h2 class="font-pixelify text-3xl font-bold">Project Head</h2>
				<div class="avatar">
					<div class="ring-offset-cv-primary w-36 rounded-full ring-4 ring-white ring-offset-2">
						<img src={`${blobStoreUrl}/images/team/mahaswetha.png`} alt="cv_dept_head" />
					</div>
				</div>
				<p class="font-inria-sans text-3xl font-bold">Mahaswetha S</p>
			</div>
		</div>

		<div class="flex min-h-screen flex-col gap-y-2 md:h-screen">
			<h1 class="font-bebas pt-12 pb-0 text-center text-7xl md:text-8xl">Our Projects</h1>

			<div
				class="flex w-full grow flex-col items-center justify-center gap-y-10 p-5 md:flex-row md:gap-x-4 md:gap-y-0"
			>
				<div class="card bg-cv-accent md:h-[60%] md:w-[40%]">
					<div class="card-body">
						<h2 class="card-title font-kanit text-3xl">Obstacle avoidance robot</h2>
						<p class="font-inria-sans text-lg">
							This is a robot that can detect and avoid obstacles in its path using ultrasonic
							sensors and camera vision.
						</p>
						<div class="card-actions justify-end">
							<label for="cv-proj-1" class="btn bg-cv-primary border-none text-white shadow-none"
								>Read More</label
							>
						</div>
					</div>
				</div>

				<div class="card bg-cv-accent md:h-[60%] md:w-[40%]">
					<div class="card-body">
						<h2 class="card-title font-kant text-3xl">
							Objection Detection using Thermal Imaging Camera
						</h2>
						<p class="font-inria-sans text-md">
							This project detects and classifies objects based on temperature using thermal
							imaging. A simulated version uses an Arduino and TMP36 sensor, while the real-world
							model uses a Raspberry Pi and MLX90640 sensor with YOLO for object detection.
						</p>
						<div class="card-actions justify-end">
							<label for="cv-proj-2" class="btn bg-cv-primary border-none text-white shadow-none"
								>Read More</label
							>
						</div>
					</div>
				</div>

				<div class="card bg-cv-accent md:h-[60%] md:w-[40%]">
					<div class="card-body">
						<h2 class="card-title font-kanit text-3xl">Gesture controlled device switch</h2>
						<p class="font-inria-sans text-md">
							A user wants to control a bulb in their room using hand gestures. Instead of pressing
							a traditional switch, they can use a simple hand wave or other gestures to turn the
							bulb on or off. This makes it easier to control the appliance without physically
							interacting with a switch
						</p>
						<div class="card-actions justify-end">
							<label for="cv-proj-3" class="btn bg-cv-primary border-none text-white shadow-none"
								>Read More</label
							>
						</div>
					</div>
				</div>

				<div class="card bg-cv-accent md:h-[60%] md:w-[40%]">
					<div class="card-body">
						<h2 class="card-title font-kanit text-3xl">Face Detection based door lock</h2>
						<p class="font-inria-sans text-md">
							This project uses a camera and face recognition algorithm to identify authorized
							individuals in real-time. A Raspberry Pi unlocks the door for recognized faces using a
							relay and solenoid lock
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

	.cv-card-title {
		view-transition-name: var(--cv-title-text);
	}
</style>
