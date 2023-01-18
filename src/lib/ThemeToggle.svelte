<script lang="ts">
	// relies on script in app.html
	import { onMount } from 'svelte'
	import { slide } from 'svelte/transition'
	let theme: string | null

	onMount(() => {
		theme = localStorage.getItem('theme')
	})

	function toggleTheme() {
		document.documentElement.classList.toggle('dark')
		if (theme === 'dark') {
			theme = 'light'
			localStorage.setItem('theme', 'light')
			return
		}
		theme = 'dark'
		localStorage.setItem('theme', 'dark')
	}
</script>

<button
	on:click={toggleTheme}
	class="rounded flex bg-nord5 h-10 p-2 top-10 right-10 w-10 absolute dark:bg-nord3">
	<iconify-icon
		icon={theme == 'dark' ? 'tabler:moon' : 'tabler:sun'}
		class="animate-fast text-2xl"
		class:animate-wobble={theme == 'dark'}
		class:animate-swing={theme == 'light'}
		transition:slide />
</button>
