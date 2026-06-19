<script>
	let regions = [
		{
			icon: '🌍',
			title: 'West Africa',
			desc: "Nigeria, Ghana, Senegal, Côte d'Ivoire, and across ECOWAS — agro-processing, manufacturing, services export"
		},
		{
			icon: '🌏',
			title: 'East & Southern Africa',
			desc: 'Kenya, Ethiopia, Tanzania, South Africa — AfCFTA corridors, light manufacturing, agricultural export'
		},
		{
			icon: '🌐',
			title: 'North Africa',
			desc: 'Egypt, Morocco, Tunisia — continental hubs, financial institutions, SEZ financing'
		},
		{
			icon: '🏝',
			title: 'Caribbean',
			desc: 'CARICOM countries — Caribbean Development Fund partnerships, diaspora SME finance, trade facilitation'
		}
	];
</script>

<section id="reach">
	<div class="reach-inner">
		<div class="reach-left">
			<div class="section-tag light">Continental Reach</div>
			<h2 class="section-h light">Capital Flows Where<br /><em>It's Needed Most.</em></h2>
			<p class="reach-p">
				From Casablanca to Cape Town, from Lagos to Kingston — the work spans the full breadth of
				the African continent and reaches into the Caribbean.
			</p>
		</div>
		<div class="reach-right">
			{#each regions as r}
				<div class="reach-item">
					<div class="reach-item-icon">{r.icon}</div>
					<div>
						<div class="reach-item-title">{r.title}</div>
						<div class="reach-item-desc">{r.desc}</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>

<style>
	#reach {
		position: relative;
		background: var(--navy2);
		padding: 8rem 6vw;
		overflow: hidden;
	}
	.reach-inner {
		position: relative;
		z-index: 2;
		max-width: 1200px;
		margin: 0 auto;
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
	.reach-p {
		font-size: 1rem;
		font-weight: 300;
		color: rgba(255, 255, 255, 0.55);
		line-height: 1.85;
		margin-top: 1.5rem;
	}
	.reach-right {
		display: flex;
		flex-direction: column;
		gap: 1.2rem;
	}
	.reach-item {
		display: flex;
		gap: 1.4rem;
		align-items: flex-start;
		padding: 1.4rem 1.6rem;
		background: rgba(255, 255, 255, 0.04);
		border: 1px solid rgba(196, 137, 58, 0.15);
		border-radius: 4px;
		transition:
			background 0.3s,
			border-color 0.3s;
	}
	.reach-item:hover {
		background: rgba(196, 137, 58, 0.07);
		border-color: rgba(196, 137, 58, 0.3);
	}
	.reach-item-icon {
		width: 40px;
		height: 40px;
		flex-shrink: 0;
		background: rgba(196, 137, 58, 0.12);
		border-radius: 4px;
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 1.1rem;
	}
	.reach-item-title {
		font-size: 0.9rem;
		font-weight: 600;
		color: #fff;
		margin-bottom: 0.3rem;
	}
	.reach-item-desc {
		font-size: 0.82rem;
		font-weight: 300;
		color: rgba(255, 255, 255, 0.45);
		line-height: 1.55;
	}
	@media (max-width: 1000px) {
		.reach-inner {
			grid-template-columns: 1fr;
			gap: 3rem;
		}
	}
</style>
