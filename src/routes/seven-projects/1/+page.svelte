<script lang="ts">
	import SevenLayout from '../_RSC/SevenLayout.svelte';
	let count = $state(0);
</script>

{#snippet description()}
	<p>A simple counter component.</p>
{/snippet}

{#snippet content()}
	<input class="rounded" disabled type="text" bind:value={count} />
	<button class="px-4 py-2 bg-stone-400 text-white rounded" onclick={() => count++}
		>Increment</button
	>
{/snippet}

<SevenLayout title="Increment" {description} {content} />
