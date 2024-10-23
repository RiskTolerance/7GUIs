<script lang="ts">
	import type { Snippet } from 'svelte';

	let { children } = $props();
</script>

<div class="w-full flex flex-col gap-8">
	<ul class="flex gap-8">
		<a href="/seven-projects/1"><li>1. Counter</li></a>
		<a href="/seven-projects/2-1"><li>2. Temperature Conversion</li></a>
		<a href="/seven-projects/2-2"><li>2.1 Temperature Conversion</li></a>
		<a href="/seven-projects/3"><li>Three</li></a>
		<a href="/seven-projects/4"><li>Four</li></a>
		<a href="/seven-projects/5"><li>Five</li></a>
		<a href="/seven-projects/6"><li>Six</li></a>
		<a href="/seven-projects/7"><li>Seven</li></a>
	</ul>

	{@render children()}
</div>
