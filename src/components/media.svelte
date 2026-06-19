<script>
	let items = [
		{
			source: 'The Guardian Nigeria',
			title: '"SMEs Must Diversify Innovatively to Survive"',
			desc: 'On why African SMEs must move beyond traditional sectors and embrace export-orientation.',
			num: '01',
			big: true
		},
		{
			source: 'This Day Live',
			title: '"Education & Access to Information Critical for SME Survival"',
			desc: 'Why financial literacy and credit information access remain underrated factors in SME survival.',
			num: '02',
			big: false
		},
		{
			source: 'EFInA Podcast',
			title: 'Credit Literacy, Personal Finance & Financial Health',
			desc: 'On the state of financial health in Nigeria and how institutions can better serve the mass market.',
			num: '03',
			big: false
		},
		{
			source: 'Daily Post · Nairametrics',
			title: '"Making Nigeria a Credit-Driven Society" (Parts 1 & 2)',
			desc: 'Two-part series on structural barriers to credit access and needed systemic changes.',
			num: '04',
			big: false
		},
		{
			source: 'LinkedIn Long-Form',
			title: '"Access to Credit: A Neglected Piece"',
			desc: "The missing link in Nigeria's development conversation.",
			num: '05',
			big: false
		}
	];
</script>

<section id="media">
	<div class="media-inner">
		<div class="section-head">
			<div class="section-tag light">Insights & Media</div>
			<h2 class="section-h light">In Print.<br /><em>On Record.</em></h2>
		</div>
		<div class="media-grid">
			{#each items as m}
				<div class="media-tile" class:media-tile--big={m.big}>
					<div class="media-source">{m.source}</div>
					<div class="media-title">{m.title}</div>
					<p class="media-desc">{m.desc}</p>
					<div class="media-corner-num">{m.num}</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<style>
	#media {
		background: var(--navy);
		padding: 8rem 6vw;
		overflow: hidden;
	}
	.media-inner {
		max-width: 1200px;
		margin: 0 auto;
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
	.media-grid {
		display: grid;
		grid-template-columns: 2fr 1fr 1fr;
		grid-template-rows: auto auto;
		gap: 1.5px;
		background: rgba(196, 137, 58, 0.12);
		margin-top: 4rem;
	}
	.media-tile {
		background: var(--navy2);
		padding: 2.2rem 2rem;
		position: relative;
		overflow: hidden;
		transition: background 0.3s;
	}
	.media-tile:hover {
		background: var(--navy3);
	}
	.media-tile--big {
		grid-row: span 2;
		padding: 3rem 2.5rem;
	}
	.media-source {
		font-size: 0.64rem;
		font-weight: 700;
		letter-spacing: 0.18em;
		text-transform: uppercase;
		color: var(--gold2);
		display: flex;
		align-items: center;
		gap: 0.6rem;
		margin-bottom: 1.4rem;
	}
	.media-source::before {
		content: '';
		width: 20px;
		height: 1.5px;
		background: var(--gold);
	}
	.media-title {
		font-family: var(--serif);
		font-size: 1.15rem;
		font-weight: 600;
		color: #fff;
		line-height: 1.35;
		margin-bottom: 0.9rem;
	}
	.media-tile--big .media-title {
		font-size: 1.6rem;
	}
	.media-desc {
		font-size: 0.84rem;
		font-weight: 300;
		color: rgba(255, 255, 255, 0.45);
		line-height: 1.7;
	}
	.media-corner-num {
		position: absolute;
		right: 1.5rem;
		bottom: 1rem;
		font-family: var(--serif);
		font-size: 5rem;
		font-weight: 700;
		color: rgba(255, 255, 255, 0.03);
	}
	@media (max-width: 1000px) {
		.media-grid {
			grid-template-columns: 1fr;
		}
		.media-tile--big {
			grid-row: span 1;
		}
	}
</style>
