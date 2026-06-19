<script>
	let stats = [
		{ num: 'US$600M+', label: 'SME Pipeline Built' },
		{ num: '54', label: 'African Markets' },
		{ num: '20+', label: 'Years in Finance' }
	];
</script>

<section id="hero">
	<div class="hero-grad-l"></div>
	<div class="hero-grad-b"></div>
	<div class="hero-inner">
		<div class="hero-eyebrow">
			<div class="eyebrow-bar"></div>
			<span class="eyebrow-text">Lagos · Cairo · 54 African Markets · Caribbean</span>
		</div>

		<h1 class="hero-name">
			<strong>Jerry</strong>
			<em>Osagie.</em>
		</h1>

		<div class="hero-divider"></div>

		<p class="hero-sub">
			<strong>Export Finance. SME Development. Continent-Scale Impact.</strong><br />
			Two decades moving capital to the businesses Africa needs most. Author. Speaker. Institution Builder.
		</p>

		<div class="hero-ctas">
			<a href="#about" class="cta-p">Discover My Story <span>↓</span></a>
			<a href="#contact" class="cta-g">Let's Connect</a>
		</div>
	</div>

	<div class="hero-chips">
		{#each stats as s}
			<div class="chip">
				<span class="chip-num">{s.num}</span>
				<span class="chip-label">{s.label}</span>
			</div>
		{/each}
	</div>

	<div class="scroll-hint">
		<div class="scroll-line"></div>
		<span>Scroll to explore</span>
	</div>
</section>

<style>
	#hero {
		position: relative;
		height: 100vh;
		min-height: 680px;
		display: flex;
		align-items: center;
		overflow: hidden;
		background: var(--navy);
	}
	.hero-grad-l {
		position: absolute;
		inset: 0;
		background: linear-gradient(90deg, var(--navy) 38%, transparent 75%);
		z-index: 1;
	}
	.hero-grad-b {
		position: absolute;
		bottom: 0;
		left: 0;
		right: 0;
		height: 35%;
		background: linear-gradient(to top, var(--navy), transparent);
		z-index: 1;
	}
	.hero-inner {
		position: relative;
		z-index: 3;
		padding: 0 6vw;
		max-width: 1320px;
		width: 100%;
		margin: 0 auto;
		padding-top: 70px;
	}
	.hero-eyebrow {
		display: flex;
		align-items: center;
		gap: 0.9rem;
		margin-bottom: 2rem;
	}
	.eyebrow-bar {
		width: 40px;
		height: 1px;
		background: var(--gold);
	}
	.eyebrow-text {
		font-size: 0.68rem;
		font-weight: 600;
		letter-spacing: 0.22em;
		text-transform: uppercase;
		color: var(--gold2);
	}
	.hero-name {
		font-family: var(--serif);
		font-size: clamp(4rem, 9vw, 8.5rem);
		font-weight: 300;
		line-height: 0.92;
		color: #fff;
		margin-bottom: 1.2rem;
	}
	.hero-name strong {
		display: block;
		font-weight: 700;
		color: #fff;
	}
	.hero-name em {
		display: block;
		font-style: italic;
		color: var(--gold2);
		font-weight: 300;
	}
	.hero-divider {
		width: 64px;
		height: 1.5px;
		background: linear-gradient(90deg, var(--gold), transparent);
		margin: 2rem 0;
	}
	.hero-sub {
		font-size: clamp(0.95rem, 1.5vw, 1.15rem);
		font-weight: 300;
		color: rgba(255, 255, 255, 0.6);
		line-height: 1.8;
		max-width: 480px;
		margin-bottom: 3rem;
	}
	.hero-sub strong {
		color: rgba(255, 255, 255, 0.9);
		font-weight: 500;
	}
	.hero-ctas {
		display: flex;
		gap: 1.2rem;
		flex-wrap: wrap;
	}
	.cta-p {
		display: inline-flex;
		align-items: center;
		gap: 0.6rem;
		background: var(--gold);
		color: var(--navy);
		font-size: 0.78rem;
		font-weight: 700;
		letter-spacing: 0.12em;
		text-transform: uppercase;
		text-decoration: none;
		padding: 0.85rem 2rem;
		border-radius: 1px;
		transition:
			background 0.2s,
			transform 0.2s;
	}
	.cta-p:hover {
		background: var(--gold2);
		transform: translateY(-2px);
	}
	.cta-g {
		display: inline-flex;
		align-items: center;
		gap: 0.6rem;
		background: transparent;
		color: rgba(255, 255, 255, 0.8);
		font-size: 0.78rem;
		font-weight: 500;
		letter-spacing: 0.12em;
		text-transform: uppercase;
		text-decoration: none;
		padding: 0.85rem 2rem;
		border-radius: 1px;
		border: 1px solid rgba(255, 255, 255, 0.22);
		transition:
			border-color 0.2s,
			color 0.2s,
			transform 0.2s;
	}
	.cta-g:hover {
		border-color: var(--gold);
		color: var(--gold2);
		transform: translateY(-2px);
	}
	.hero-chips {
		position: absolute;
		right: 6vw;
		top: 50%;
		transform: translateY(-50%);
		z-index: 3;
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}
	.chip {
		background: rgba(255, 255, 255, 0.06);
		backdrop-filter: blur(12px);
		border: 1px solid rgba(196, 137, 58, 0.25);
		border-radius: 4px;
		padding: 1.2rem 1.5rem;
		min-width: 170px;
	}
	.chip-num {
		font-family: var(--serif);
		font-size: 2.1rem;
		font-weight: 600;
		color: var(--gold2);
		line-height: 1;
		display: block;
	}
	.chip-label {
		font-size: 0.68rem;
		font-weight: 400;
		color: rgba(255, 255, 255, 0.5);
		margin-top: 0.3rem;
		display: block;
	}
	.scroll-hint {
		position: absolute;
		bottom: 2.5rem;
		left: 6vw;
		z-index: 3;
		display: flex;
		align-items: center;
		gap: 0.8rem;
	}
	.scroll-line {
		width: 1px;
		height: 48px;
		background: linear-gradient(to bottom, var(--gold), transparent);
		animation: pulse 2.5s ease-in-out infinite;
	}
	.scroll-hint span {
		font-size: 0.63rem;
		letter-spacing: 0.22em;
		text-transform: uppercase;
		color: rgba(255, 255, 255, 0.3);
	}
	@keyframes pulse {
		0%,
		100% {
			opacity: 0.3;
		}
		50% {
			opacity: 1;
		}
	}
	@media (max-width: 1000px) {
		.hero-chips {
			display: none;
		}
	}
</style>
