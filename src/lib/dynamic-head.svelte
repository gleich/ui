<script lang="ts">
	import { page } from '$app/state';

	let {
		title,
		description,
		siteName,
		opengraphImage = {
			url: 'https://mattglei.ch/opengraph.png',
			width: '1200',
			height: '630'
		},
		keywords = [],
		iconRoot = 'https://mattglei.ch'
	}: {
		title: string;
		description: string;
		siteName: string;
		opengraphImage?: OpenGraphImage;
		keywords?: string[];
		iconRoot?: string;
	} = $props();

	export interface OpenGraphImage {
		url: string;
		width: string;
		height: string;
	}

	keywords = keywords.concat([
		'matt gleich',
		'matt',
		'gleich',
		'matthew gleich',
		'matthew',
		'gleich',
		'photography',
		'coding',
		'cycling',
		'rit',
		'stainless',
		'bottomline technologies',
		'kcf technologies',
		'kcf'
	]);
</script>

<svelte:head>
	<title>{title}</title>
	<link rel="canonical" href={page.url.href.replaceAll('http://', 'https://').replace(/\/$/, '')} />
	<meta name="description" content={description} />
	<meta name="url" content={page.url.href} />

	<meta name="author" content="Matt Gleich" />
	<meta name="keywords" content={keywords.join(', ')} />

	<!-- icons -->
	<link rel="apple-touch-icon" href={`${iconRoot}/apple-touch-icon.png`} sizes="180x180" />
	<link
		rel="icon"
		type="image/png"
		sizes="192x192"
		href={`${iconRoot}/android-chrome-192x192.png`}
	/>
	<link
		rel="icon"
		type="image/png"
		sizes="512x512"
		href={`${iconRoot}/android-chrome-512x512.png`}
	/>
	<link rel="icon" href={`${iconRoot}/favicon-32x32.png`} sizes="32x32" />
	<link rel="icon" href={`${iconRoot}/favicon-16x16.png`} sizes="16x16" />
	<link rel="mask-icon" href={`${iconRoot}/safari-pinned-tab.svg`} color="#292B2D" />
	<link rel="icon" href={`${iconRoot}/favicon.ico`} />

	<!-- opengraph -->
	<meta property="og:title" content={title} />
	<meta property="og:description" content={description} />
	<meta property="og:url" content={page.url.href} />
	<meta property="og:site_name" content={siteName} />
	<meta property="og:locale" content="en-US" />
	<meta property="og:image" content={opengraphImage.url} />
	<meta property="og:image:width" content={opengraphImage.width} />
	<meta property="og:image:height" content={opengraphImage.height} />
	<meta property="og:type" content="website" />

	<!-- twitter -->
	<meta property="twitter:card" content="summary_large_image" />
	<meta property="twitter:creator" content="@matt_gleich" />
	<meta property="twitter:title" content={title} />
	<meta property="twitter:description" content={description} />
	<meta property="twitter:image" content={opengraphImage.url} />
	<meta property="twitter:image:width" content={opengraphImage.width} />
	<meta property="twitter:image:height" content={opengraphImage.height} />
</svelte:head>
