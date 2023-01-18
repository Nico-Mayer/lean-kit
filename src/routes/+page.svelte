<script lang="ts">
	import 'iconify-icon'
	let shadow = false

	function toggleShadow() {
		shadow = !shadow
	}
</script>

<section class="flex flex-col m-auto space-y-10 items-center">
	<div
		class="rounded flex bg-nord6 h-50 shadow-nord15 w-50 dark:bg-nord3 "
		class:shadow-xl={shadow}>
		<h1 class="font-bold m-auto">lean-kit</h1>
	</div>
	<button
		class="rounded flex bg-nord5 h-10 p-2 w-10 gap-2 items-center dark:bg-nord2"
		on:click={toggleShadow}>
		<iconify-icon
			icon={!shadow ? 'tabler:shadow-off' : 'tabler:shadow'}
			class:animate-wobble={shadow}
			class:animate-swing={!shadow}
			class="animate-fast text-2xl " />
	</button>
</section>
