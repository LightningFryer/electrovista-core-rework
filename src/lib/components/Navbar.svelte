<script lang="ts">
	import Navrail from './Navrail.svelte';
	let openNavrailComponent = false;
	import gsap from 'gsap';
</script>

<nav class="fixed z-20 flex h-20 max-w-screen min-w-screen bg-[#3A6351]/80 shadow-2xl shadow-black">
	<div class="flex flex-col">
		<!-- svelte-ignore a11y_no_static_element_interactions -->
		<!-- svelte-ignore a11y_click_events_have_key_events -->
		<div
			class="flex h-full w-full flex-row items-center justify-start pl-6"
			onmouseenter={() => (openNavrailComponent = true)}
			onmouseleave={() => (openNavrailComponent = false)}
			onclick={() => !openNavrailComponent}
		>
			<a
				href="/"
				class="navbar-logo btn btn-circle size-16 rounded-full border-none bg-white p-6 text-black transition-[scale] duration-300 hover:scale-105 hover:bg-yellow-300 hover:text-white"
				>*LOGO*</a
			>
		</div>
		<div><Navrail navrailOpen={openNavrailComponent} /></div>
	</div>
</nav>
