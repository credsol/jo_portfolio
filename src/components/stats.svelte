<script>
	let stats = [
		{
			icon: '🌍',
			num: 'US$600M',
			suffix: '+',
			desc: 'SME export finance pipeline built across Africa and the Caribbean at Afreximbank'
		},
		{
			icon: '💰',
			num: 'US$35M',
			suffix: '+',
			desc: 'Institutional income generated through the SME financing portfolio at Afreximbank'
		},
		{
			icon: '🗺',
			num: '54',
			suffix: '',
			desc: 'African markets and Caribbean territories covered under the Afreximbank SME mandate'
		},
		{
			icon: '🏦',
			num: 'US$1B',
			suffix: '+',
			desc: 'Total credit deployed across a career spanning commercial banking, fintech, and development finance'
		},
		{
			icon: '📱',
			num: '3.5M',
			suffix: '+',
			desc: 'Credit applications processed via digital platform at NIRSAL Microfinance Bank within 15 months'
		},
		{
			icon: '👥',
			num: '300K',
			suffix: '+',
			desc: 'Entrepreneurs supported through SME finance, capacity building, and development programmes'
		}
	];
</script>

<section id="stats">
	<div class="stats-bg-text">AFRICA</div>
	<div class="stats-inner">
		<div class="stats-label">Impact in Numbers</div>
		<div class="stats-grid">
			{#each stats as s}
				<div class="stat-card">
					<span class="stat-icon">{s.icon}</span>
					<span class="stat-num"><b>{s.num}</b>{s.suffix}</span>
					<p class="stat-desc">{s.desc}</p>
				</div>
			{/each}
		</div>
	</div>
</section>

<style>
	#stats {
		background: var(--navy);
		padding: 7rem 6vw;
		position: relative;
		overflow: hidden;
	}
	.stats-bg-text {
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		font-family: var(--serif);
		font-size: clamp(8rem, 18vw, 22rem);
		font-weight: 700;
		color: rgba(255, 255, 255, 0.02);
		white-space: nowrap;
		pointer-events: none;
	}
	.stats-inner {
		position: relative;
		z-index: 2;
		max-width: 1200px;
		margin: 0 auto;
	}
	.stats-label {
		font-size: 0.7rem;
		font-weight: 700;
		letter-spacing: 0.2em;
		text-transform: uppercase;
		color: var(--gold);
		display: flex;
		align-items: center;
		gap: 0.8rem;
		margin-bottom: 4rem;
	}
	.stats-label::after {
		content: '';
		flex: 1;
		height: 1px;
		background: rgba(196, 137, 58, 0.25);
	}
	.stats-grid {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: 0;
	}
	.stat-card {
		padding: 3.5rem 3rem;
		border-right: 1px solid rgba(196, 137, 58, 0.12);
		border-bottom: 1px solid rgba(196, 137, 58, 0.12);
		position: relative;
		transition: background 0.4s;
	}
	.stat-card:hover {
		background: rgba(196, 137, 58, 0.05);
	}
	.stat-card:nth-child(3n) {
		border-right: none;
	}
	.stat-card:nth-child(4),
	.stat-card:nth-child(5),
	.stat-card:nth-child(6) {
		border-bottom: none;
	}
	.stat-num {
		font-family: var(--serif);
		font-size: clamp(3rem, 5vw, 4.5rem);
		font-weight: 300;
		color: #fff;
		line-height: 1;
		display: block;
		margin-bottom: 0.6rem;
	}
	.stat-num b {
		color: var(--gold2);
	}
	.stat-desc {
		font-size: 0.88rem;
		font-weight: 300;
		color: rgba(255, 255, 255, 0.45);
		line-height: 1.65;
		max-width: 220px;
	}
	.stat-icon {
		position: absolute;
		right: 1.5rem;
		top: 1.5rem;
		font-size: 1.8rem;
		opacity: 0.15;
	}
	@media (max-width: 1000px) {
		.stats-grid {
			grid-template-columns: 1fr 1fr;
		}
		.stat-card:nth-child(2n) {
			border-right: none;
		}
		.stat-card:nth-child(2n + 1) {
			border-right: 1px solid rgba(196, 137, 58, 0.12);
		}
		.stat-card:nth-child(5),
		.stat-card:nth-child(6) {
			border-bottom: none;
		}
	}
</style>
