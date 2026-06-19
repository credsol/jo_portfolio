<script>
	let cards = [
		{
			icon: '🌍',
			title: 'Export Finance & Trade',
			body: 'Structuring and delivering export credit facilities, trade finance instruments, and intermediated lending programmes across African and Caribbean markets — across 54 markets and growing. Active co-financing relationships with World Bank Group, IFC, EIB, China Development Bank, USAID, and the Caribbean Development Fund.',
			num: '01',
			featured: true
		},
		{
			icon: '📊',
			title: 'SME Ecosystem Development',
			body: 'Designing and operationalising SME financing programmes at institutional scale — credit frameworks, technical assistance, and impact measurement.',
			num: '02',
			featured: false
		},
		{
			icon: '🏦',
			title: 'Development Finance Institutions',
			body: 'Deep familiarity with DFI governance, multilateral co-financing structures, and the full investment lifecycle at continental scale.',
			num: '03',
			featured: false
		},
		{
			icon: '💳',
			title: 'Credit Risk & Policy',
			body: '14 years of commercial banking credit discipline — SME credit policy, portfolio quality, NPL reduction, and credit disbursement at scale.',
			num: '04',
			featured: false
		},
		{
			icon: '📱',
			title: 'Digital Finance & Fintech',
			body: 'Designed and oversaw digital lending platforms processing millions of applications nationally. Climate and renewable energy finance certified.',
			num: '05',
			featured: false
		}
	];
</script>

<section id="expertise">
	<div class="expertise-inner">
		<div class="section-head">
			<div class="section-tag">What I Do</div>
			<h2 class="section-h">Deep Expertise.<br /><em>Proven Execution.</em></h2>
		</div>
		<div class="expertise-grid">
			{#each cards as c}
				<div class="exp-card" class:exp-card--featured={c.featured}>
					<div class="exp-card-icon">{c.icon}</div>
					<div class="exp-card-title">{c.title}</div>
					<p class="exp-card-body">{c.body}</p>
					<div class="exp-card-num">{c.num}</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<style>
	#expertise {
		background: var(--cream);
		padding: 8rem 6vw;
	}
	.expertise-inner {
		max-width: 1200px;
		margin: 0 auto;
	}
	.expertise-grid {
		display: grid;
		grid-template-columns: 2fr 1fr 1fr;
		grid-template-rows: auto auto;
		gap: 1.5px;
		background: rgba(196, 137, 58, 0.2);
	}
	.exp-card {
		background: var(--white);
		padding: 2.8rem 2.4rem;
		position: relative;
		overflow: hidden;
		transition: background 0.3s;
	}
	.exp-card:hover {
		background: #fafafa;
	}
	.exp-card--featured {
		grid-row: span 2;
		background: var(--navy);
	}
	.exp-card--featured:hover {
		background: var(--navy2);
	}
	.exp-card-icon {
		width: 44px;
		height: 44px;
		border-radius: 4px;
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 1.3rem;
		margin-bottom: 2rem;
		background: rgba(196, 137, 58, 0.1);
	}
	.exp-card--featured .exp-card-icon {
		background: rgba(196, 137, 58, 0.15);
	}
	.exp-card-title {
		font-family: var(--serif);
		font-size: 1.35rem;
		font-weight: 600;
		line-height: 1.2;
		margin-bottom: 0.9rem;
		color: var(--navy);
	}
	.exp-card--featured .exp-card-title {
		color: #fff;
		font-size: 1.7rem;
	}
	.exp-card-body {
		font-size: 0.88rem;
		font-weight: 300;
		line-height: 1.75;
		color: var(--mid);
	}
	.exp-card--featured .exp-card-body {
		color: rgba(255, 255, 255, 0.55);
	}
	.exp-card-num {
		position: absolute;
		bottom: 2rem;
		right: 2rem;
		font-family: var(--serif);
		font-size: 5rem;
		font-weight: 700;
		color: rgba(196, 137, 58, 0.08);
	}
	.exp-card--featured .exp-card-num {
		color: rgba(255, 255, 255, 0.04);
		font-size: 9rem;
	}
	@media (max-width: 1000px) {
		.expertise-grid {
			grid-template-columns: 1fr;
		}
		.exp-card--featured {
			grid-row: span 1;
		}
	}
</style>
