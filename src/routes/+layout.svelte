<script lang="ts">
	import type { Snippet } from 'svelte';
	import '../lib/styles.css';
	import './global.css';
	import Layout from '$lib/layout.svelte';

	const { children }: { children: Snippet } = $props();
</script>

<Layout repo="gleich/ui">
	{@render children()}
</Layout>
