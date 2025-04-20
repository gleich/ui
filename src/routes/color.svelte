<script lang="ts">
	const { variable }: { variable: string } = $props();
</script>

<div class="container">
	<div class="demo" style={`background-color: var(${variable})`}></div>
	<p>{variable}</p>
</div>

<style>
	.container {
		display: flex;
		align-items: center;
		gap: 10px;
	}

	.demo {
		width: 20px;
		height: 20px;
		border-radius: 5px;
		border: 1px solid var(--border);
	}
</style>
