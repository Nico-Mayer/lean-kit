<script lang="ts">
	import '../app.css'
	import { activeTheme } from '$lib/stores/store'
	import { onMount } from 'svelte'

	onMount(() => {
		const localTheme = localStorage.getItem('theme')

		switch (localTheme) {
			case 'dark':
				$activeTheme = 'dark'
				break
			case 'light':
				$activeTheme = 'light'
				break
			default:
				$activeTheme = 'dark'
				break
		}
	})
</script>

<slot />
