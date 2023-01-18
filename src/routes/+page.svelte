<script lang="ts">
	import 'iconify-icon'
	let shadow = false

	function toggleShadow() {
		shadow = !shadow
	}
</script>

<section class="flex flex-col m-auto space-y-10 items-center">
	<div class="bg-white rounded flex h-50 w-50" class:shadow-xl={shadow}>
		<h1 class="font-bold m-auto text-nord3">lean-kit</h1>
	</div>
	<button
		class="rounded flex bg-nord4 p-2 text-red-500 gap-2 items-center"
		on:click={toggleShadow}>
		<iconify-icon
			icon={!shadow ? 'tabler:shadow-off' : 'tabler:shadow'}
			class:animate-wobble={shadow}
			class:animate-swing={!shadow}
			class="animate-fast text-2xl text-nord0" />
	</button>
</section>
