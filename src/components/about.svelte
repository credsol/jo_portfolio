<script lang="ts">
	import { asset } from '$app/paths';
</script>

<section id="about">
	<div class="about-top">
		<div class="about-image-col">
			<div class="about-img-bg">
				<img class="image" src={asset('/images/jerry_osagie.webp')} alt="Jerry Osagie" />
			</div>
			<div class="about-img-caption">
				<p>"I build financing ecosystems that move capital to the businesses Africa needs most."</p>
				<span>Jerry Osagie — Lagos, Nigeria</span>
			</div>
		</div>

		<div class="about-text-col">
			<div class="about-label">The Story</div>
			<h2 class="about-h">Finance as a<br /><em>Force for Growth.</em></h2>

			<p class="about-p">
				Over <strong>two decades</strong>, I have worked at the intersection of commercial banking
				discipline, development finance impact, and SME ecosystem leadership.
			</p>

			<blockquote class="about-quote">
				Capital is not just money. It is possibility. My life's work is to make that possibility
				real for African entrepreneurs.
			</blockquote>

			<p class="about-p">
				From the credit floors of <strong>Diamond Bank</strong> to the executive layers of
				continental development finance at <strong>Afreximbank</strong>, every chapter has deepened
				one conviction: Africa's economic potential is constrained not by ambition, but by access.
			</p>

			<div class="about-ctas">
				<a href="#contact" class="cta-p navy">Start a Conversation</a>
				<a
					href="https://www.linkedin.com/in/jerry-osagie-84708323"
					target="_blank"
					rel="noopener"
					class="cta-g navy"
				>
					View LinkedIn
				</a>
			</div>
		</div>
	</div>
</section>

<style>
	#about {
		background: var(--white);
		overflow: hidden;
	}
	.about-top {
		display: grid;
		grid-template-columns: 1fr 1fr;
		min-height: 90vh;
	}
	.about-image-col {
		position: relative;
		overflow: hidden;
		min-height: 600px;
	}
	.about-img-bg {
		background: linear-gradient(160deg, var(--navy2) 0%, var(--navy3) 40%, #1a3a6e 100%);
		width: 100%;
		height: 100%;
		display: 'flex';
		justify-items: center;
		justify-content: center;
	}
	.about-img-caption {
		position: absolute;
		bottom: 2rem;
		left: 2rem;
		right: 2rem;
		background: rgba(8, 23, 46, 0.85);
		backdrop-filter: blur(8px);
		border-left: 3px solid var(--gold);
		padding: 1.1rem 1.4rem;
	}
	.about-img-caption p {
		font-family: var(--serif);
		font-size: 1.05rem;
		font-style: italic;
		color: rgba(255, 255, 255, 0.9);
		line-height: 1.55;
	}
	.about-img-caption span {
		font-size: 0.68rem;
		letter-spacing: 0.12em;
		text-transform: uppercase;
		color: var(--gold2);
		display: block;
		margin-top: 0.4rem;
	}
	.about-text-col {
		padding: 7vw 5vw 7vw 6vw;
		display: flex;
		flex-direction: column;
		justify-content: center;
	}
	.about-label {
		font-size: 0.68rem;
		font-weight: 700;
		letter-spacing: 0.2em;
		text-transform: uppercase;
		color: var(--gold);
		margin-bottom: 1.5rem;
		display: flex;
		align-items: center;
		gap: 0.8rem;
	}
	.about-label::before {
		content: '';
		width: 32px;
		height: 1px;
		background: var(--gold);
	}
	.about-h {
		font-family: var(--serif);
		font-size: clamp(2.4rem, 3.5vw, 3.6rem);
		font-weight: 600;
		line-height: 1.1;
		color: var(--navy);
		margin-bottom: 2rem;
	}
	.about-h em {
		font-style: italic;
		color: var(--gold);
	}
	.about-p {
		font-size: 1rem;
		font-weight: 300;
		color: var(--mid);
		line-height: 1.85;
		margin-bottom: 1.1rem;
	}
	.about-p strong {
		color: var(--navy);
		font-weight: 600;
	}
	.about-quote {
		font-family: var(--serif);
		font-size: 1.35rem;
		font-style: italic;
		color: var(--navy);
		line-height: 1.55;
		border-left: 3px solid var(--gold);
		padding-left: 1.5rem;
		margin: 2.5rem 0;
	}
	.about-ctas {
		display: flex;
		gap: 1rem;
		flex-wrap: wrap;
		margin-top: 2rem;
	}
	.cta-p.navy {
		background: var(--navy);
		color: var(--white);
		padding: 5px;
		border-radius: 5px;
	}
	.cta-g.navy {
		border-color: rgba(8, 23, 46, 0.22);
		color: var(--navy);
	}
	.image {
		padding-top: 10px;
		border-radius: 5px;
	}
	@media (max-width: 1000px) {
		.about-top {
			grid-template-columns: 1fr;
		}
		.about-image-col {
			min-height: 380px;
			max-height: 603px;
		}
	}
</style>
