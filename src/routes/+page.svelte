<script>
	import Card from '$lib/card.svelte';
	import Copyright from '$lib/copyright.svelte';
	import DynamicHead from '$lib/dynamic-head.svelte';
	import Error from '$lib/error.svelte';
	import Image from '$lib/image.svelte';
	import Logo from '$lib/logo.svelte';
	import NavLogo from '$lib/nav-logo.svelte';
	import Scrolling from '$lib/scrolling.svelte';
	import Color from './color.svelte';
</script>

<DynamicHead
	title="gleich/ui"
	description="Shared UI components used across a number of my personal projects."
/>

<main>
	<div class="title">
		<div class="logo">
			<NavLogo />
		</div>

		<h1>@gleich/ui</h1>
	</div>

	<p class="description">
		Shared <a href="https://svelte.dev" target="_blank">Svelte</a> components used across a number of
		my personal projects.
	</p>

	<section>
		<h2>Colors</h2>

		<div class="colors">
			<Color variable="--green-foreground" />
			<Color variable="--green-border" />
			<Color variable="--green-background" />

			<Color variable="--red-foreground" />
			<Color variable="--red-background" />
			<Color variable="--red-border" />

			<Color variable="--button-background" />
			<Color variable="--border" />
			<Color variable="--background" />
			<Color variable="--actual-background-color" />

			<Color variable="--blue-foreground" />
		</div>
	</section>

	<section>
		<h2>&lt;a&gt;&lt;/a&gt;</h2>
		<a href="https://mattglei.ch" target="_blank">mattglei.ch</a>
	</section>

	<section>
		<h2>&lt;Button/&gt;</h2>
		<button class="button-demo">Demo</button>
	</section>

	<section>
		<h2>&lt;Error/&gt;</h2>
		<Error msg="Error demo" />
	</section>

	<section>
		<h2>&lt;Image/&gt;</h2>
		<Image
			src="https://mattglei.ch/opengraph.png"
			width={1200}
			height={630}
			alt="Opengraph demo image"
		/>
	</section>

	<section>
		<h2>&lt;Layout&gt;&lt;/Layout&gt;</h2>
		<p>
			Causes the entire page to fade up, aligns the content to the middle, makes the width max out
			at 1040px, and adds padding in all directions.
		</p>
	</section>

	<section>
		<h2>&lt;Scrolling/&gt;</h2>
		<div class="scrolling-demo">
			<Scrolling>This text scrolls when the text element overflows</Scrolling>
		</div>
	</section>

	<section>
		<h2>&lt;Card/&gt;</h2>
		<Card>
			<p>Card</p>
		</Card>
	</section>

	<section>
		<h2>&lt;Copyright/&gt;</h2>
		<Copyright repo="gleich/ui" />
	</section>

	<section>
		<h2>&lt;Logo/&gt;</h2>
		<div class="logo-demo">
			<Logo />
		</div>
	</section>

	<section>
		<h2>&lt;NavLogo/&gt;</h2>
		<NavLogo />
	</section>
</main>

<style>
	section {
		border: 1px solid var(--border);
		padding: 10px;
		margin: 20px 0;
		box-shadow: var(--box-shadow);
		border-radius: var(--border-radius);
		background-color: var(--background);
	}

	section h2 {
		margin-bottom: 20px;
	}

	.description {
		margin-top: 20px;
	}

	.title {
		display: flex;
		gap: 20px;
		align-items: center;
	}

	.colors {
		display: flex;
		flex-wrap: wrap;
		gap: 10px;
	}

	.button-demo {
		padding: 10px 20px;
	}

	.scrolling-demo {
		width: 200px;
	}

	.logo-demo {
		width: 100px;
		height: 100px;
	}

	@font-face {
		font-family: 'IBM Plex Mono';
		src: url('/fonts/ibm_plex_mono/bold.woff2');
		font-weight: 700;
		font-display: swap;
	}

	@font-face {
		font-family: 'IBM Plex Mono';
		src: url('/fonts/ibm_plex_mono/medium.woff2');
		font-weight: 500;
		font-display: swap;
	}

	@font-face {
		font-family: 'IBM Plex Mono';
		src: url('/fonts/ibm_plex_mono/normal.woff2');
		font-weight: 400;
		font-display: swap;
	}

	@font-face {
		font-family: 'IBM Plex Sans';
		src: url('/fonts/ibm_plex_sans/medium.woff2');
		font-weight: 500;
		font-display: swap;
	}

	@font-face {
		font-family: 'Inter';
		src: url('/fonts/inter/bold.woff2');
		font-weight: 700;
		font-display: swap;
	}

	@font-face {
		font-family: 'Inter';
		src: url('/fonts/inter/extra_bold.woff2');
		font-weight: 800;
		font-display: swap;
	}
</style>
