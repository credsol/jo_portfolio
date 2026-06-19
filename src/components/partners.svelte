<script>
	let partners = [
		'World Bank Group',
		'International Finance Corporation (IFC)',
		'European Investment Bank',
		'African Development Bank',
		'China Development Bank',
		'USAID',
		'UNDP',
		'Caribbean Development Fund',
		"Women's World Banking",
		'Bank of Industry, Nigeria',
		'Central Bank of Nigeria',
		'African Union Commission',
		'COMESA',
		'ECOWAS',
		'Africa CEO Forum',
		'OECD SME Finance Platform'
	];
</script>

<section id="partners">
	<div class="partners-inner">
		<div class="section-tag">Institutional Relationships</div>
		<h2 class="section-h">Bridging Capital<br /><em>&amp; Ambition.</em></h2>
		<p class="partners-lead">
			Active working relationships with the multilateral institutions, development banks, and
			government bodies that shape Africa's financial architecture.
		</p>
		<div class="partners-grid">
			{#each partners as p}
				<div class="partner-pill">{p}</div>
			{/each}
		</div>
	</div>
</section>

<style>
	#partners {
		background: var(--cream);
		padding: 7rem 6vw;
	}
	.partners-inner {
		max-width: 1200px;
		margin: 0 auto;
	}
	.partners-lead {
		font-size: 0.98rem;
		font-weight: 300;
		color: var(--mid);
		max-width: 560px;
		line-height: 1.75;
		margin-bottom: 3rem;
		margin-top: 1rem;
	}
	.partners-grid {
		display: flex;
		flex-wrap: wrap;
		gap: 0.8rem;
	}
	.partner-pill {
		font-size: 0.78rem;
		font-weight: 500;
		color: var(--navy);
		background: var(--white);
		border: 1px solid rgba(8, 23, 46, 0.12);
		padding: 0.55rem 1.3rem;
		border-radius: 100px;
		transition:
			background 0.2s,
			color 0.2s,
			border-color 0.2s;
	}
	.partner-pill:hover {
		background: var(--navy);
		color: var(--gold2);
		border-color: var(--navy);
	}
</style>
