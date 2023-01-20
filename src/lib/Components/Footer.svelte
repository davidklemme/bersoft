<script>
	let isMenuOpen = false;
</script>
<style>
	.footer {
		width: calc(100%);
		}
</style>

<footer 
    class="footer p-4
    bg-neutral text-secondary text-xs 
    flex items-center justify-between">
	<div>
		2023 | Berliner Softwareschmiede 
	</div>
	<div class="hidden md:flex items-center font-bold">
		<a href="/impressum">Impressum</a>
		<div class="dropdown dropdown-top dropdown-end" class:dropdown-open={isMenuOpen}>
			<label tabIndex={0} class="btn m-1">Kontakt</label>
			<ul tabIndex={0} class="dropdown-content menu p-2 shadow bg-base-200 rounded-box w-52 text-secondary">
				<li><a>Mail</a></li>
				<li><a>Datenschutz & Privacy</a></li>
			  </ul>
		</div>
		<!-- <a href="/contact">Kontakt</a> -->
	</div>
	<div class="md:hidden">
		<div class="dropdown dropdown-top" class:dropdown-open={isMenuOpen}>
			<label tabIndex={0} class="btn m-1 text-xs">Impressum</label>
			<ul tabIndex={0} class="dropdown-content menu p-2 shadow bg-base-100 rounded-box w-52 ">
				<li><a>Mail</a></li>
				<li><a>Impressum</a></li>
			  </ul>
		</div>

	</div>

</footer>