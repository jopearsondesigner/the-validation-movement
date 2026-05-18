<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();
</script>

<svelte:head>
	<title>The Validation Movement</title>

	<meta
		name="description"
		content="A compassion-centered platform dedicated to reducing the stigma surrounding Borderline Personality Disorder through emotionally intelligent design, supportive tools, education, and lived experience."
	/>

	<link rel="icon" href="/favicon/favicon.svg" type="image/svg+xml" />

	<link rel="alternate icon" href="/favicon/favicon-32.png" type="image/png" />

	<link rel="apple-touch-icon" href="/favicon/apple-touch-icon.png" />
</svelte:head>

{@render children()}
