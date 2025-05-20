<script lang="ts">
	import type { Snippet } from 'svelte';
	import '../lib/styles.css';
	import './global.css';
	import Layout from '$lib/layout.svelte';
	import { siteName } from '$lib/sitename.js';

	siteName.set('ui.mattglei.ch');

	const { children }: { children: Snippet } = $props();
</script>

<Layout repo="gleich/ui">
	{@render children()}
</Layout>
