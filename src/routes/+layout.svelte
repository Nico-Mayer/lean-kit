<script lang="ts">
	import '../app.css'
	import 'virtual:windi.css'
	import 'iconify-icon'
	import ThemeToggle from '$lib/ThemeToggle.svelte'
</script>

<main
	class="flex h-screen bg-nord4 w-screen text-nord0 relative dark:bg-nord0 dark:text-nord6">
	<ThemeToggle />
	<slot />
</main>
