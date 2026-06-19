<script>
	import { onMount } from 'svelte';
	let scrolled = false;

	onMount(() => {
		const onScroll = () => (scrolled = window.scrollY > 60);
		window.addEventListener('scroll', onScroll);
		return () => window.removeEventListener('scroll', onScroll);
	});

	function smoothTo(id) {
		document.querySelector(id)?.scrollIntoView({ behavior: 'smooth', block: 'start' });
	}
</script>

<nav class:on={scrolled}>
	<a href="#hero" class="nav-logo" on:click|preventDefault={() => smoothTo('#hero')}>
		Jerry <b>Osagie</b>
	</a>
	<div class="flex items-center justify-center gap-2.5">
		<ul class="nav-links">
			<li><a href="#about" on:click|preventDefault={() => smoothTo('#about')}>Story</a></li>
			<li>
				<a href="#expertise" on:click|preventDefault={() => smoothTo('#expertise')}>Expertise</a>
			</li>
			<li>
				<a href="#speaking" on:click|preventDefault={() => smoothTo('#speaking')}>Speaking</a>
			</li>
			<li><a href="#books" on:click|preventDefault={() => smoothTo('#books')}>Books</a></li>
			<li><a href="#media" on:click|preventDefault={() => smoothTo('#media')}>Insights</a></li>
		</ul>
		<a href="#contact" class="nav-btn" on:click|preventDefault={() => smoothTo('#contact')}
			>Connect</a
		>
	</div>
</nav>

<style>
	nav {
		position: fixed;
		top: 0;
		left: 0;
		right: 0;
		z-index: 200;
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 0 6vw;
		height: 70px;
		background: var(--navy);
		transition:
			background 0.5s,
			border-color 0.5s;
	}
	nav.on {
		background: rgba(8, 23, 46, 0.96);
		backdrop-filter: blur(16px);
		border-bottom: 1px solid rgba(196, 137, 58, 0.18);
	}
	.nav-logo {
		font-family: var(--serif);
		font-size: 1.3rem;
		font-weight: 600;
		color: #fff;
		text-decoration: none;
		letter-spacing: 0.02em;
	}
	.nav-logo b {
		color: var(--gold2);
		font-weight: 700;
	}
	.nav-links {
		display: flex;
		gap: 2.5rem;
		list-style: none;
	}

	@media (max-width: 1000px) {
		.nav-links {
			display: none;
		}
	}

	.nav-links a {
		font-size: 0.72rem;
		font-weight: 500;
		letter-spacing: 0.14em;
		text-transform: uppercase;
		color: rgba(255, 255, 255, 0.65);
		text-decoration: none;
		transition: color 0.2s;
	}
	.nav-links a:hover {
		color: var(--gold2);
	}
	.nav-btn {
		font-size: 0.72rem;
		font-weight: 700;
		letter-spacing: 0.12em;
		text-transform: uppercase;
		color: var(--navy);
		background: var(--gold);
		padding: 0.5rem 1.4rem;
		border-radius: 1px;
		text-decoration: none;
		transition:
			background 0.2s,
			transform 0.2s;
	}
	.nav-btn:hover {
		background: var(--gold2);
		transform: translateY(-1px);
	}
</style>
