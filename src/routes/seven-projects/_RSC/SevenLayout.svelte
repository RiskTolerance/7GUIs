<script lang="ts">
	import type { Snippet } from 'svelte';
	const {
		title,
		description,
		content
	}: { title: string; description?: Snippet; content?: Snippet } = $props();
</script>

<div class="my-8 space-y-8">
	<span class="prose space-y-8">
		<h1>{title}</h1>
		{#if description}
			{@render description()}
		{/if}
	</span>
	{#if content}
		<div>
			{@render content()}
		</div>
	{/if}
</div>
