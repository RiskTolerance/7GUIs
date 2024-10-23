<script lang="ts">
	import Navigation from '$lib/components/Navigation.svelte';
	import '../app.css';
	let { children } = $props();
</script>

<Navigation></Navigation>
<div class="w-full bg-stone-50">
	<div class="container mx-auto flex justify-center ">
	{@render children()}
</div>
</div>

