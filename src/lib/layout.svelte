<script lang="ts">
	import type { Snippet } from 'svelte';
	import Copyright from './copyright.svelte';

	const { children, repo, fill = true }: { children: Snippet; repo: string; fill?: boolean } = $props();
</script>

<div class="container">
	<div class="main" class:fill>
		<div class="page-content">
			{@render children()}
		</div>
		<div class="copyright">
			<Copyright {repo} />
		</div>
	</div>
</div>

<style>
	.container {
		display: flex;
		align-items: center;
		flex-direction: column;
		min-height: 100vh;
		overflow: hidden;
	}

	.main {
		display: flex;
		flex-direction: column;
		width: 100%;
		max-width: 1040px;
		padding: 70px 20px;
	}

	.main.fill {
		flex: 1;
	}

	.page-content {
		flex: 1;
	}

	.copyright {
		margin-top: 20px;
		width: 100%;
	}

	@media (max-width: 450px) {
		.main {
			padding: 50px 10px;
		}
	}
</style>
