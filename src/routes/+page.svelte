<script lang="ts">
	import tvmLogo from '$lib/assets/logos/tvm-logo-primary.svg';
</script>

<svelte:head>
	<title>The Validation Movement</title>
	<meta
		name="description"
		content="A compassion-centered platform dedicated to reducing the stigma surrounding Borderline Personality Disorder through emotionally intelligent design, supportive tools, education, and lived experience."
	/>
</svelte:head>

<main class="page-shell">
	<header class="site-header">
		<img src={tvmLogo} alt="The Validation Movement" class="site-logo" />
	</header>

	<section class="hero">
		<div class="eyebrow">
			<span></span>
			CORE BELIEF
		</div>

		<h1 class="hero-heading">
			BPD is not
			<span class="hero-emphasis">“too much.”</span>
		</h1>

		<div class="hero-divider"></div>

		<div class="hero-content">
			<div class="hero-statement">
				<p>
					It is often overwhelming emotional pain being communicated in the only language someone
					has.
				</p>
			</div>

			<div class="hero-support">
				<p>
					A compassion-centered platform dedicated to reducing stigma surrounding Borderline
					Personality Disorder through emotionally intelligent design, supportive tools, education,
					and lived experience.
				</p>

				<div class="hero-actions">
					<a href="#for-bpd" class="ghost-button primary"> I Have BPD </a>

					<a href="#understand-bpd" class="ghost-button"> I Want to Understand BPD </a>
				</div>
			</div>
		</div>
	</section>

	<section class="belief-strip">
		<div class="belief-item">
			<span>Validation is not agreement.</span>
		</div>

		<div class="belief-item">
			<span>Intensity is not manipulation.</span>
		</div>

		<div class="belief-item">
			<span>Pain is not attention-seeking.</span>
		</div>
	</section>

	<section class="editorial-message">
		<div class="eyebrow">
			<span></span>
			EMOTIONAL REALITY
		</div>

		<div class="editorial-grid">
			<h2>People are not asking to be dramatic.</h2>

			<div class="editorial-copy">
				<p>
					They are trying to communicate something real, frightening, and overwhelming — often
					without the regulation, safety, or emotional language they needed growing up.
				</p>

				<p>
					The Validation Movement exists to create understanding before judgment, regulation before
					shame, and emotional safety before explanation.
				</p>
			</div>
		</div>
	</section>

	<section class="principles-grid">
		<article class="principle-card">
			<span class="principle-number">01</span>

			<h3>Believe the intensity.</h3>

			<p>The emotion may seem impossible from the outside. That does not mean it is exaggerated.</p>
		</article>

		<article class="principle-card">
			<span class="principle-number">02</span>

			<h3>Reduce shame.</h3>

			<p>
				Validation begins by making emotional experience understandable instead of treating it like
				a character flaw.
			</p>
		</article>

		<article class="principle-card">
			<span class="principle-number">03</span>

			<h3>Offer regulation.</h3>

			<p>
				Support should lower cognitive load and help someone return to safety before asking them to
				explain themselves.
			</p>
		</article>
	</section>

	<section class="featured-tool">
		<div class="eyebrow">
			<span></span>
			FEATURED TOOL
		</div>

		<div class="tool-layout">
			<div class="tool-copy">
				<h2>Calm Now</h2>

				<p>
					A focused emotional regulation experience designed for moments of panic, spiraling,
					overwhelm, rejection sensitivity, or attachment activation.
				</p>

				<a href="/calm-now" class="ghost-button primary"> Open The Tool </a>
			</div>

			<div class="tool-preview">
				<div class="preview-screen">
					<div class="preview-pulse"></div>

					<p class="preview-text">Self is here.</p>
				</div>
			</div>
		</div>
	</section>
</main>
