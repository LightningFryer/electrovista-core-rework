<script>
	let { navrailOpen = false } = $props();
</script>

<aside
	onmouseenter={() => (navrailOpen = true)}
	onmouseleave={() => (navrailOpen = false)}
	class="absolute z-20 flex {navrailOpen
		? 'translate-x-[0%]'
		: 'translate-x-[-100%]'} max-h-screen min-h-screen bg-black p-8 transition-[translate] duration-200 ease-in-out"
>
	<div class="flex h-full flex-col items-center justify-center gap-3">
		<a
			class="btn rounded-full border-none bg-white p-6 text-black transition-[scale] duration-300 hover:scale-105 hover:bg-yellow-300 hover:text-white"
			>Home</a
		>
		<a
			class="btn rounded-full border-none bg-white p-6 text-black transition-[scale] duration-300 hover:scale-105 hover:bg-yellow-300 hover:text-white"
			>Projects</a
		>
		<a
			class="btn rounded-full border-none bg-white p-6 text-black transition-[scale] duration-300 hover:scale-105 hover:bg-yellow-300 hover:text-white"
			>Team</a
		>
		<a
			class="btn rounded-full border-none bg-white p-6 text-black transition-[scale] duration-300 hover:scale-105 hover:bg-yellow-300 hover:text-white"
			>Contact</a
		>
	</div>
</aside>
