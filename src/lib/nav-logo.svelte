<script lang="ts">
	import Logo from './logo.svelte';

	const { width = '50px', height = width }: { width?: string; height?: string } = $props();
</script>

<div class="logo" style:--width={width} style:--height={height}>
	<Logo stroke="6" />
</div>

<style>
	.logo {
		width: var(--width);
		height: var(--height);
		border: 1px solid var(--border);
		box-shadow: inset var(--box-shadow);
		background-color: var(--background);
		border-radius: var(--border-radius);
		padding: 3px;
	}
</style>
