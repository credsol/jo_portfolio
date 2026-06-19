<script>
	let topics = [
		"Export Finance & AfCFTA — Converting Africa's Trade Potential",
		"SME Access to Finance — What Works, What Doesn't",
		'Credit Culture & Financial Literacy in Emerging Markets',
		'Digital Finance & The Future of Credit Access in Africa',
		'Women & Youth Entrepreneurship — Financing the Next Generation',
		'DFI & Private Sector Partnership in African Trade'
	];

	let engagements = [
		{
			year: '2025',
			title: 'EU-Africa SME Summit, Johannesburg',
			org: 'European Union — Africa Business'
		},
		{
			year: '2025',
			title: 'African Development Bank Annual Meeting — Vision 2030 Fund',
			org: 'African Development Bank Group'
		},
		{
			year: '2025',
			title: 'Nigerian National MSME Conference',
			org: 'SMEDAN / Federal Government of Nigeria'
		},
		{ year: '2024', title: 'OECD Global SME Finance Forum', org: 'OECD · São Paulo, Brazil' },
		{
			year: '2024',
			title: 'Pan-Africa Job Creation — Africa CEO Forum',
			org: 'Africa CEO Forum, Abidjan'
		},
		{
			year: '2023',
			title: 'AU Commission ASMED 3P Expert Working Group',
			org: 'African Union Commission'
		},
		{
			year: '2023',
			title: '14th African Congress for Women Entrepreneurs, Cairo',
			org: 'COMESA Businesswomen'
		},
		{
			year: '2021',
			title: 'Youth Entrepreneurship Financing — IATF',
			org: 'Intra-African Trade Fair · Durban, South Africa'
		}
	];
</script>

<section id="speaking">
	<div class="speaking-hero">
		<div class="speaking-hero-inner">
			<div class="speaking-hero-text">
				<div class="section-tag light">On the Stage</div>
				<h2 class="section-h light">
					Speaking at the<br /><em>Intersection of Finance,<br />Policy &amp; Africa.</em>
				</h2>
				<p class="speaking-hero-p">
					The speaking is grounded in lived experience — having built the programmes, led the
					institutions, and structured the transactions I speak about.
				</p>
			</div>
			<div class="speaking-topics-list">
				{#each topics as t}
					<div class="speaking-topic-item">
						<div class="topic-bullet"></div>
						<div class="topic-name">{t}</div>
					</div>
				{/each}
			</div>
		</div>
	</div>

	<div class="engagements-wrap">
		<div class="section-tag">Selected Engagements</div>
		<div class="eng-grid">
			{#each engagements as e}
				<div class="eng-card">
					<div class="eng-year">{e.year}</div>
					<div class="eng-info">
						<div class="eng-title">{e.title}</div>
						<div class="eng-org">{e.org}</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<style>
	#speaking {
		background: var(--white);
		overflow: hidden;
	}
	.speaking-hero {
		position: relative;
		min-height: 55vh;
		background: var(--navy);
		display: flex;
		align-items: center;
		overflow: hidden;
	}
	.speaking-hero-inner {
		position: relative;
		z-index: 2;
		max-width: 1200px;
		margin: 0 auto;
		padding: 5rem 6vw;
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 6rem;
		align-items: center;
	}
	.section-tag.light {
		color: var(--gold2);
	}
	.section-tag.light::before {
		background: var(--gold2);
	}
	.section-h.light {
		color: #fff;
	}
	.section-h.light em {
		color: var(--gold2);
	}
	.speaking-hero-p {
		font-size: 1rem;
		font-weight: 300;
		color: rgba(255, 255, 255, 0.55);
		line-height: 1.85;
		margin-top: 1.5rem;
	}
	.speaking-topics-list {
		display: flex;
		flex-direction: column;
		gap: 0.7rem;
	}
	.speaking-topic-item {
		display: flex;
		align-items: center;
		gap: 1rem;
		padding: 0.9rem 1.2rem;
		background: rgba(255, 255, 255, 0.05);
		border: 1px solid rgba(196, 137, 58, 0.15);
		border-radius: 3px;
		transition:
			background 0.25s,
			border-color 0.25s;
	}
	.speaking-topic-item:hover {
		background: rgba(196, 137, 58, 0.08);
		border-color: rgba(196, 137, 58, 0.3);
	}
	.topic-bullet {
		width: 5px;
		height: 5px;
		background: var(--gold);
		border-radius: 50%;
		flex-shrink: 0;
	}
	.topic-name {
		font-size: 0.88rem;
		font-weight: 400;
		color: rgba(255, 255, 255, 0.8);
	}
	.engagements-wrap {
		padding: 6rem 6vw;
		max-width: 1200px;
		margin: 0 auto;
	}
	.eng-grid {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: 1.2rem;
		margin-top: 3rem;
	}
	.eng-card {
		display: flex;
		gap: 1.2rem;
		padding: 1.4rem;
		border: 1px solid rgba(8, 23, 46, 0.08);
		border-radius: 4px;
		transition:
			transform 0.25s,
			box-shadow 0.25s;
	}
	.eng-card:hover {
		transform: translateY(-3px);
		box-shadow: 0 12px 40px rgba(8, 23, 46, 0.08);
	}
	.eng-year {
		font-family: var(--serif);
		font-size: 1rem;
		font-weight: 600;
		color: var(--gold);
		min-width: 38px;
		padding-top: 0.1rem;
	}
	.eng-title {
		font-size: 0.9rem;
		font-weight: 600;
		color: var(--navy);
		line-height: 1.35;
		margin-bottom: 0.25rem;
	}
	.eng-org {
		font-size: 0.78rem;
		font-weight: 300;
		color: var(--soft);
	}
	@media (max-width: 1000px) {
		.speaking-hero-inner {
			grid-template-columns: 1fr;
			gap: 3rem;
		}
		.eng-grid {
			grid-template-columns: 1fr;
		}
	}
</style>
