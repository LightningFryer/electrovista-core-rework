<script>
	let { navrailOpen = false } = $props();
</script>

<aside
	onmouseenter={() => (navrailOpen = true)}
	onmouseleave={() => (navrailOpen = false)}
	class="absolute z-20 flex {navrailOpen
		? 'translate-x-[0%]'
		: 'translate-x-[-100%]'} max-h-screen min-h-screen bg-[#3A6351]/80 p-8 transition-[translate] duration-200 ease-in-out"
>
	<div class="flex h-full flex-col items-center justify-center gap-3">
		<a
			class="btn btn-lg font-kanit min-w-fit w-36 cursor-pointer rounded-full font-light shadow-none hover:border-[#3A6351] hover:bg-[#3A6351] hover:text-white"
			>Home</a
		>
		<a
			class="btn btn-lg font-kanit min-w-fit w-36 cursor-pointer rounded-full font-light shadow-none hover:border-[#3A6351] hover:bg-[#3A6351] hover:text-white"
			>Departments</a
		>
		<a
			class="btn btn-lg font-kanit min-w-fit w-36 cursor-pointer rounded-full font-light shadow-none hover:border-[#3A6351] hover:bg-[#3A6351] hover:text-white"
			>Team</a
		>
		<a
			class="btn btn-lg font-kanit min-w-fit w-36 cursor-pointer rounded-full font-light shadow-none hover:border-[#3A6351] hover:bg-[#3A6351] hover:text-white"
			>Contact</a
		>
	</div>
</aside>
