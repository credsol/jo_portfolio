<script>
	let items = [
		'Export Finance',
		'SME Development',
		'Africa & Caribbean',
		'54 Markets',
		'Development Finance',
		'Trade Finance',
		'Author',
		'Speaker',
		'Institution Builder',
		'AfCFTA',
		'Lagos · Cairo'
	];
</script>

<div class="marquee-wrap">
	<div class="marquee-track">
		{#each [0, 1] as _}
			<div class="marquee-item">
				{#each items as item}
					{item} <span class="marquee-dot"></span>
				{/each}
			</div>
		{/each}
	</div>
</div>

<style>
	.marquee-wrap {
		background: var(--gold);
		overflow: hidden;
		padding: 0.75rem 0;
	}
	.marquee-track {
		display: flex;
		width: max-content;
		animation: marquee 28s linear infinite;
	}
	.marquee-item {
		white-space: nowrap;
		padding: 0 2.5rem;
		font-size: 0.72rem;
		font-weight: 700;
		letter-spacing: 0.16em;
		text-transform: uppercase;
		color: var(--navy);
		display: flex;
		align-items: center;
		gap: 2.5rem;
	}
	.marquee-dot {
		width: 4px;
		height: 4px;
		background: var(--navy);
		border-radius: 50%;
		opacity: 0.4;
		display: inline-block;
	}
	@keyframes marquee {
		to {
			transform: translateX(-50%);
		}
	}
</style>
