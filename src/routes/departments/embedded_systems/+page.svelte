<script lang="ts">
	import type { PageData } from './$types';

	let { data }: { data: PageData } = $props();
</script>

<main
	class="dotted-background-wrapper text-purple flex h-screen flex-col items-center justify-center !bg-[#F1B81A]"
>
	<div class="flex h-full w-full flex-col">
		<div class="border-purple flex h-[20%] flex-col items-center justify-center p-32">
			<h1
				class="es-card-title text-purple font-bebas text-9xl"
				style:--es-title-text="es-title-text"
			>
				Embedded Systems
			</h1>
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
