<script>
	import { blobStoreUrl } from '$lib/blobStoreUrl';
	import { Instagram, Lightbulb } from 'lucide-svelte';
</script>

<footer
	class="footer md:footer-horizontal text-neutral-content z-10 bg-[#3A6351] p-10"
	id="footer-sec"
>
	<aside>
		<img
			src={`${blobStoreUrl}/images/logos/elec_full_logo.png`}
			class="h-16 w-full md:h-28 md:w-full"
			alt=""
		/>
	</aside>
	<nav>
		<h6 class="footer-title">Socials And Links</h6>
		<div class="grid grid-flow-col gap-4">
			<a
				href="https://www.instagram.com/electrovista.mitblr?igsh=MXRycmF2NWZtamMwdw%3D%3D&utm_source=qr"
				target="_blank"
			>
				<Instagram />
			</a>
			<a
				href="https://linktr.ee/ElectroVista?utm_source=linktree_profile_share&ltsid=2a58d291-186b-449a-8dde-7bc59d9a0b2b"
				target="_blank"
			>
				<Lightbulb />
			</a>
		</div>
	</nav>
</footer>
