<!-- src/routes/+page.svelte -->

<script lang="ts">
	import tvmLogo from '$lib/assets/logos/tvm-logo-primary.svg';
	import heroImage from '$lib/assets/images/tvm-hero-lilith-not-alone.webp';

	const beliefs = [
		'Validation is not agreement.',
		'Intensity is not manipulation.',
		'Pain is not attention-seeking.'
	];

	const principles = [
		{
			number: '01',
			title: 'Believe the intensity.',
			text: 'The emotion may seem impossible from the outside. That does not mean it is exaggerated.'
		},
		{
			number: '02',
			title: 'Reduce shame.',
			text: 'Validation begins by making emotional experience understandable instead of treating it like a character flaw.'
		},
		{
			number: '03',
			title: 'Offer regulation.',
			text: 'Support should lower cognitive load and help someone return to safety before asking them to explain themselves.'
		}
	];
</script>

<svelte:head>
	<title>The Validation Movement</title>
	<meta
		name="description"
		content="A compassion-centered platform dedicated to reducing the stigma surrounding Borderline Personality Disorder through emotionally intelligent design, supportive tools, education, and lived experience."
	/>
</svelte:head>

<main>
	<section class="hero-art">
		<header class="floating-header" aria-label="Site header">
			<a href="/" class="floating-logo-link" aria-label="The Validation Movement home">
				<img src={tvmLogo} alt="The Validation Movement" class="floating-logo" />
			</a>
		</header>

		<div class="hero-art-image-wrap" aria-hidden="true">
			<img src={heroImage} alt="" class="hero-art-image" />

			<div class="hero-art-overlay"></div>
			<div class="hero-art-grain"></div>
		</div>

		<div class="hero-art-content">
			<div class="hero-art-copy">
				<p class="eyebrow light">
					<span></span>
					Core belief
				</p>

				<h1 class="hero-art-heading">
					BPD is not
					<span>“too much.”</span>
				</h1>

				<p class="hero-art-statement">
					It is often overwhelming emotional pain being communicated in the only language someone
					has.
				</p>

				<div class="hero-art-actions">
					<a href="#for-bpd" class="hero-button primary"> I Have BPD </a>

					<a href="#understand-bpd" class="hero-button"> I Want to Understand BPD </a>
				</div>
			</div>
		</div>
	</section>

	<section class="cream-section">
		<div class="page-shell">
			<section class="belief-grid" aria-label="Core validation beliefs">
				{#each beliefs as belief}
					<article class="belief-card">
						<p>{belief}</p>
					</article>
				{/each}
			</section>

			<section class="editorial-message">
				<p class="eyebrow">
					<span></span>
					Emotional reality
				</p>

				<div class="editorial-grid">
					<h2>People are not asking to be dramatic.</h2>

					<div class="editorial-copy">
						<p>
							They are trying to communicate something real, frightening, and overwhelming — often
							without the regulation, safety, or emotional language they needed growing up.
						</p>

						<p>
							The Validation Movement exists to create understanding before judgment, regulation
							before shame, and emotional safety before explanation.
						</p>
					</div>
				</div>
			</section>

			<section class="principles-grid" aria-label="Validation principles">
				{#each principles as principle}
					<article class="principle-card">
						<span class="principle-number">{principle.number}</span>

						<h3>{principle.title}</h3>

						<p>{principle.text}</p>
					</article>
				{/each}
			</section>

			<section class="featured-tool">
				<p class="eyebrow">
					<span></span>
					Featured tool
				</p>

				<div class="tool-layout">
					<div class="tool-copy">
						<h2>Calm Now</h2>

						<p>
							A focused emotional regulation experience designed for moments of panic, spiraling,
							overwhelm, rejection sensitivity, or attachment activation.
						</p>

						<a href="/calm-now" class="ghost-button primary"> Open The Tool </a>
					</div>

					<div class="tool-preview" aria-hidden="true">
						<div class="preview-screen">
							<div class="preview-pulse"></div>

							<p class="preview-text">A softer place to land.</p>
						</div>
					</div>
				</div>
			</section>
		</div>
	</section>
</main>
