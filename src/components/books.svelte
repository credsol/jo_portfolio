<script>
	let books = [
		{
			year: 'Published 2019',
			title: 'Borrowing Made Easy',
			desc: 'A practical, plain-language guide to SME access to finance in emerging markets. Covers credit fundamentals, how to approach lenders, how to structure a borrowing proposition, and how to build a credit culture that works.',
			gradient: 'g1',
			link: 'https://borrowingmadeeasy.africa/'
		},
		{
			year: 'Published 2020',
			title: 'Loans: 50 Things You Need to Know',
			desc: 'A concise, power-packed reference guide covering 50 essential principles of borrowing — from understanding loan terms and interest structures to managing credit health.',
			gradient: 'g2',
			link: 'https://borrowingmadeeasy.africa/loans_50'
		}
	];
</script>

<section id="books">
	<div class="books-inner">
		<div class="section-head">
			<div class="section-tag">Published Works</div>
			<h2 class="section-h">Books That Make<br /><em>Finance Accessible.</em></h2>
		</div>
		<div class="books-grid">
			{#each books as b}
				<a href={b.link} class="book-card">
					<div class="book-visual {b.gradient}">
						<div class="book-visual-title">
							<div class="bvt-main">{b.title}</div>
							<div class="bvt-author">— Jerry Osagie</div>
						</div>
						<div class="book-gold-bar"></div>
					</div>
					<div class="book-body">
						<div class="book-year">{b.year}</div>
						<div class="book-title">{b.title}</div>
						<p class="book-desc">{b.desc}</p>
					</div>
				</a>
			{/each}
		</div>
	</div>
</section>

<style>
	#books {
		background: var(--cream);
		padding: 8rem 6vw;
	}
	.books-inner {
		max-width: 1200px;
		margin: 0 auto;
	}
	.books-grid {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 2.5rem;
		margin-top: 4rem;
	}
	.book-card {
		position: relative;
		overflow: hidden;
		border-radius: 6px;
		background: var(--white);
		box-shadow: 0 4px 24px rgba(8, 23, 46, 0.07);
		transition:
			transform 0.35s,
			box-shadow 0.35s;
	}
	.book-card:hover {
		transform: translateY(-8px);
		box-shadow: 0 24px 64px rgba(8, 23, 46, 0.13);
	}
	.book-visual {
		height: 260px;
		position: relative;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.book-visual.g1 {
		background: linear-gradient(145deg, #0f2340 0%, #c4893a 60%, #e4a84a 100%);
	}
	.book-visual.g2 {
		background: linear-gradient(145deg, #08172e 0%, #172f52 50%, #1a3d72 100%);
	}
	.book-visual-title {
		position: absolute;
		inset: 0;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		padding: 2rem;
	}
	.bvt-main {
		font-family: var(--serif);
		font-size: clamp(1.6rem, 3vw, 2.4rem);
		font-weight: 700;
		color: #fff;
		text-align: center;
		line-height: 1.15;
		text-shadow: 0 2px 16px rgba(0, 0, 0, 0.5);
	}
	.bvt-author {
		font-size: 0.78rem;
		font-weight: 400;
		color: rgba(255, 255, 255, 0.6);
		letter-spacing: 0.12em;
		margin-top: 0.7rem;
	}
	.book-gold-bar {
		position: absolute;
		bottom: 0;
		left: 0;
		right: 0;
		height: 3px;
		background: var(--gold);
	}
	.book-body {
		padding: 2rem 2rem 2.2rem;
	}
	.book-year {
		font-size: 0.68rem;
		font-weight: 700;
		letter-spacing: 0.16em;
		text-transform: uppercase;
		color: var(--gold);
		margin-bottom: 0.6rem;
	}
	.book-title {
		font-family: var(--serif);
		font-size: 1.25rem;
		font-weight: 600;
		color: var(--navy);
		margin-bottom: 0.9rem;
		line-height: 1.25;
	}
	.book-desc {
		font-size: 0.9rem;
		font-weight: 300;
		color: var(--mid);
		line-height: 1.75;
	}
	@media (max-width: 1000px) {
		.books-grid {
			grid-template-columns: 1fr;
		}
	}
</style>
