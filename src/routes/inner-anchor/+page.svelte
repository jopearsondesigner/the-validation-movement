<!-- src/routes/inner-anchor/+page.svelte -->
<script lang="ts">
	import tvmLogo from '$lib/assets/logos/tvm-logo-primary.svg';
	import lanternGlow from '$lib/assets/graphics/celestial/lantern-glow.webp';
	import { tick } from 'svelte';

	let currentStep = $state(0);
	let isChanging = $state(false);

	const steps = [
		{
			text: 'You do not need to solve your whole life right now.',
			button: 'Okay'
		},
		{
			text: 'Let’s help your nervous system settle first.',
			button: 'Breathe'
		},
		{
			text: 'Place a hand on your chest.',
			button: 'Continue'
		},
		{
			text: 'Feel your feet against the floor.',
			button: 'Continue'
		},
		{
			text: 'What you’re feeling makes sense.',
			button: 'Begin Again'
		}
	];

	async function nextStep() {
		isChanging = true;

		await tick();

		setTimeout(() => {
			if (currentStep < steps.length - 1) {
				currentStep += 1;
			} else {
				currentStep = 0;
			}

			isChanging = false;
		}, 180);
	}
</script>

<svelte:head>
	<title>InnerAnchor | The Validation Movement</title>

	<meta name="description" content="A softer place to land." />
</svelte:head>

<section class="inner-anchor">
	<header class="floating-header" aria-label="InnerAnchor header">
		<a href="/" class="floating-logo-link" aria-label="Return home">
			<img src={tvmLogo} alt="The Validation Movement" class="floating-logo" />
		</a>
	</header>

	<div class="inner-anchor-shell">
		<div class="inner-anchor-copy">
			<p class="eyebrow">
				<span></span>
				InnerAnchor
			</p>

			<h1 class="inner-anchor-heading">
				A softer
				<span>place to land.</span>
			</h1>

			<p class="inner-anchor-intro">You are not failing for feeling overwhelmed.</p>
		</div>

		<div class="inner-anchor-card">
			<img src={lanternGlow} alt="" class="inner-anchor-atmosphere" aria-hidden="true" />

			<p class:changing={isChanging} class="step-text">
				{steps[currentStep].text}
			</p>

			<div class="step-indicators" aria-hidden="true">
				{#each steps as _, index (index)}
					<div class:active={index === currentStep} class="step-dot"></div>
				{/each}
			</div>

			<button type="button" class="ghost-button primary" onclick={nextStep}>
				{steps[currentStep].button}
			</button>
		</div>
	</div>
</section>
