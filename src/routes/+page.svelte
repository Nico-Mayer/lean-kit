<script lang="ts">
	import { activeTheme } from '$lib/stores/store'

	function toggleTheme() {
		if ($activeTheme === 'dark') {
			localStorage.setItem('theme', 'light')
			document.documentElement.classList.remove('dark')
			$activeTheme = 'light'
			return
		} else {
			localStorage.setItem('theme', 'dark')
			document.documentElement.classList.add('dark')
			$activeTheme = 'dark'
			return
		}
	}
</script>

<main
	class="w-screen h-screen dark:bg-black dark:text-white flex items-center justify-center">
	<button
		class="flex items-center justify-center gap-4 border p-4 py-2 rounded-md"
		on:click={toggleTheme}>
		<span>lean-kit</span>
	</button>
</main>
