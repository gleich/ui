<script lang="ts">
	import type { Snippet } from 'svelte';
	import '../lib/styles.css';

	const { children }: { children: Snippet } = $props();
</script>

<div class="container">
	<div class="main">
		{@render children()}
	</div>
</div>

<style>
	.container {
		display: flex;
		align-items: center;
		justify-content: center;
		min-height: 100vh;
		overflow: hidden;
	}

	.main {
		display: flex;
		flex-direction: column;
		width: 100%;
		flex: 1;
		max-width: 1000px;
		padding: 0 20px;
		padding-bottom: 0;
	}
</style>
