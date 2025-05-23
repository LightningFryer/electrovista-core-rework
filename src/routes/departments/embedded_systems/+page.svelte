<script lang="ts">
	import { blobStoreUrl } from '$lib/blobStoreUrl';
	import type { PageData } from './$types';

	let { data }: { data: PageData } = $props();
</script>

<svelte:head>
	<title>Electrovista | Embedded Systems</title>
</svelte:head>

<input type="checkbox" id="es_modal_2" class="modal-toggle" />
<div class="modal flex w-full flex-col items-center justify-center" role="dialog">
	<div class="modal-box flex h-[95%] !w-[95%] !max-w-full flex-col gap-y-7 md:!w-[60%]">
		<h3 class="font-kanit text-center text-4xl font-bold">
			Hardware-Assisted Encryption for Resource-Constrained Devices
		</h3>
		<div class="font-inria-sans flex flex-col gap-y-5 text-2xl">
			<p>
				Our hardware encryption solution implements AES-256 for resource-constrained environments,
				utilizing dedicated hardware acceleration to offload cryptographic operations from host
				systems
			</p>

			<h3 class="font-kanit text-center text-2xl font-semibold">Architecture Overview</h3>

			<p>
				The device employs a heterogeneous computing architecture combining an STM32 F401RE NUCLEO
				microcontroller with a Xilinx Artix-7 Nexys A7-50T FPGA module, all housed in a Gavin's
				Hooli box-styled encasement. This configuration provides superior performance compared to
				software-based encryption solutions while maintaining minimal power consumption
			</p>

			<h3 class="font-kanit text-center text-2xl font-semibold">Technical Implementation</h3>
			<p class="">Hardware Components</p>
			<ul class="list-disc p-6">
				<li class="text-lg">
					<span class="font-semibold">STM32 F401RE NUCLEO MCU</span>: Manages control flow and I/O
					operations
				</li>
				<li class="text-lg">
					<span class="font-semibold">Xilinx Artix-7 Nexys A7-50T FPGA</span>: Implements dedicated
					cryptographic processing units
				</li>
				<li class="text-lg">
					<span class="font-semibold">STM32 F401RE NUCLEO MCU</span>: Manages control flow and I/O
					operations
				</li>
			</ul>

			<p class="">Encryption Pipeline</p>
			<ul class="list-disc p-6">
				<li class="text-lg">
					<span class="font-semibold">Key Expansion Unit</span>: Generates round keys using
					non-linear S-box transformations
				</li>
				<li class="text-lg">
					<span class="font-semibold">SubBytes Operation</span>: Implements lookup table (LUT) based
					substitution for optimal timing
				</li>
				<li class="text-lg">
					<span class="font-semibold">ShiftRows/MixColumns</span>: Utilizes parallel processing with
					register transfer level (RTL) optimizations
				</li>
				<li class="text-lg">
					<span class="font-semibold">AddRoundKey</span>: Performs bitwise XOR operations between
					state and round key
				</li>
			</ul>
			<p>
				The design leverages SystemVerilog parameterized modules with clock domain crossing (CDC)
				synchronizers to ensure reliable data transfer between the MCU and FPGA domains.
			</p>

			<p class="">Encryption Pipeline</p>
			<ul class="list-disc p-6">
				<li>Hardware-isolated key storage prevents exposure to software vulnerabilities</li>
				<li>Side-channel attack countermeasures including constant-time operations</li>
				<li>Physical tamper detection circuitry with automatic key zeroization</li>
				<li>True hardware random number generator (TRNG) for key generation</li>
			</ul>
		</div>
		<div class="modal-action">
			<label for="es_modal_2" class="btn hover:btn-error">Close!</label>
		</div>
	</div>
</div>

<input type="checkbox" id="es_modal_1" class="modal-toggle" />
<div class="modal flex w-full flex-col items-center justify-center" role="dialog">
	<div class="modal-box flex h-[95%] !w-[95%] !max-w-full flex-col gap-y-7 md:!w-[60%]">
		<h3 class="font-kanit text-center text-4xl font-bold">
			Hybrid Terrestrial-Satellite IoT Network via CubeSats
		</h3>
		<div class="font-inria-sans flex flex-col items-center justify-center gap-y-5 text-2xl">
			<img
				src={`${blobStoreUrl}/images/dept_images/es/es-proj-1.jpg`}
				class="h-[40rem] w-[30rem]"
				alt=""
			/>
			<p>
				This project integrates terrestrial communication technologies (such as cellular, Wi-Fi, and
				LoRaWAN) with CubeSat-based satellite communication to create a hybrid IoT network. Designed
				to ensure reliable and seamless data transmission across remote and urban environments, the
				system dynamically switches between ground and satellite networks based on performance,
				cost, and availability. Key features include intelligent path selection, seamless handover,
				and load balancing—making it ideal for applications in environmental monitoring, smart
				agriculture, disaster response, and smart cities.
			</p>

			<p>
				The team visited ART GARAGE(ART Park) which is an affiliation of IISC They had gone with the
				proposal to ask for funding, guidance and collaboration with industry professionals.
			</p>
		</div>
		<div class="modal-action">
			<label for="es_modal_1" class="btn hover:btn-error">Close!</label>
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
					src={`${blobStoreUrl}/images/logos/es_base_logo.png`}
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
					<div class="ring-purple ring-offset-es-primary w-36 rounded-full ring-4 ring-offset-2">
						<img src={`${blobStoreUrl}/images/team/sumedh.png`} alt="es_dept_head" />
					</div>
				</div>
				<p class="font-inria-sans text-3xl font-bold">Sumedh Prabhudeshai</p>
			</div>
		</div>

		<div class="flex min-h-screen flex-col gap-y-2 md:h-screen">
			<h1 class="font-bebas pt-12 pb-0 text-center text-7xl md:text-8xl">Our Projects</h1>

			<div
				class="flex w-full grow flex-col items-center justify-center gap-x-4 gap-y-10 p-5 md:flex-row md:gap-y-0 md:p-6"
			>
				<div class="card bg-es-accent md:h-[60%] md:w-[40%]">
					<div class="card-body">
						<h2 class="card-title font-kanit text-3xl">
							Hybrid Terrestrial-Satellite IoT Network via CubeSats
						</h2>
						<p class="font-inria-sans text-lg">
							This project integrates terrestrial communication technologies (such as cellular,
							Wi-Fi, and LoRaWAN) with CubeSat-based satellite communication to create a hybrid IoT
							network.
						</p>
						<div class="card-actions justify-end">
							<!-- <button class="btn bg-es-primary border-none shadow-none">Read More!</button> -->
							<label for="es_modal_1" class="btn bg-es-primary border-none shadow-none"
								>Read More</label
							>
						</div>
					</div>
				</div>

				<div class="card bg-es-accent md:h-[60%] md:w-[40%]">
					<div class="card-body">
						<h2 class="card-title font-kanit text-3xl">
							Hardware-Assisted Encryption for Resource-Constrained Devices
						</h2>
						<p class="font-inria-sans text-lg">
							Our hardware encryption solution implements AES-256 for resource-constrained
							environments, utilizing dedicated hardware acceleration to offload cryptographic
							operations from host systems
						</p>
						<div class="card-actions justify-end">
							<label for="es_modal_2" class="btn bg-es-primary border-none shadow-none"
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
