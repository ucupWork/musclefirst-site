<script lang="ts">
	import { fly } from 'svelte/transition';
	export let url = '';
	const pageTransitionDuration = 500;
</script>

{#key url}
	<div
		class="relative w-full h-full m-0 flex flex-col"
		in:fly={{ y: -20, duration: pageTransitionDuration, delay: pageTransitionDuration }}
		out:fly={{ y: 20, duration: pageTransitionDuration }}
	>
		<slot />
	</div>
{/key}