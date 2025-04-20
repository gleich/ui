<script>
	import Logo from '$lib/logo.svelte';

</script>

<div class="title">
<div class="logo">
    <Logo/>
</div>

<h1>gleich/ui</h1>

</div>

<style>
    .logo {
        width: 60px;
        height: 60px;
        border: 1px solid var(--border);
        box-shadow: var(--box-shadow);
        border-radius: var(--border-radius);
        background-color: var(--background);
        padding: 3px;
    }

    .title {
        display: flex;
        gap: 20px;
        align-items: center;
    }
</style>