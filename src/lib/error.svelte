<script lang="ts">
	const { msg }: { msg: string } = $props();
</script>

<div class="container">
	<svg
		xmlns="http://www.w3.org/2000/svg"
		width="24"
		height="24"
		viewBox="0 0 24 24"
		fill="none"
		stroke="currentColor"
		stroke-width="2"
		stroke-linecap="round"
		stroke-linejoin="round"
		><polygon points="7.86 2 16.14 2 22 7.86 22 16.14 16.14 22 7.86 22 2 16.14 2 7.86 7.86 2"
		></polygon><line x1="12" y1="8" x2="12" y2="12"></line><line x1="12" y1="16" x2="12.01" y2="16"
		></line></svg
	>
	<h1>{msg}</h1>
</div>

<style>
	svg {
		height: 40px;
		width: auto;
		animation: blink 1s infinite;
	}

	h1 {
		font-size: 25px;
		font-family: 'IBM Plex Sans';
	}

	.container {
		display: flex;
		align-items: center;
		gap: 20px;
		background-color: var(--red-background);
		color: var(--red-foreground);
		padding: 30px;
		border-radius: var(--border-radius);
		border: 1px solid var(--red-border);
	}

	@-webkit-keyframes blink {
		0%,
		70% {
			opacity: 100%;
		}
		80%,
		100% {
			opacity: 30%;
		}
	}

	@keyframes blink {
		0%,
		70% {
			opacity: 100%;
		}
		80%,
		100% {
			opacity: 30%;
		}
	}
</style>
