<script lang="ts">
	import type { Snippet } from 'svelte';
	import Copyright from './copyright.svelte';

	const { children, repo }: { children: Snippet; repo: string } = $props();
</script>

<div class="container">
	<div class="children">
		{@render children()}
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

	.children {
		display: flex;
		box-sizing: border-box;
		align-items: center;
		flex-direction: column;
		width: 100%;
		animation: fade-up 0.5s ease-out forwards;
		opacity: 0;
		flex: 1;
		max-width: 1040px;
		padding: 70px 20px;
	}

	.copyright {
		margin-top: 20px;
		width: 100%;
	}

	@-webkit-keyframes fade-up {
		from {
			opacity: 0;
			transform: translateY(10px);
		}
		to {
			opacity: 1;
			transform: translateY(0);
		}
	}

	@keyframes fade-up {
		from {
			opacity: 0;
			transform: translateY(10px);
		}
		to {
			opacity: 1;
			transform: translateY(0);
		}
	}
</style>
