<script lang="ts">
	import { onMount } from 'svelte';

	let mx = 0,
		my = 0,
		rx = 0,
		ry = 0;

	let cur, curR;

	onMount(() => {
		const onMove = (e) => {
			mx = e.clientX;
			my = e.clientY;
			cur.style.left = mx + 'px';
			cur.style.top = my + 'px';
		};
		window.addEventListener('mousemove', onMove);

		let raf;
		const loop = () => {
			rx += (mx - rx) * 0.11;
			ry += (my - ry) * 0.11;
			curR.style.left = rx + 'px';
			curR.style.top = ry + 'px';
			raf = requestAnimationFrame(loop);
		};
		loop();

		const hoverables = document.querySelectorAll(
			'a,button,.stat-card,.exp-card,.book-card,.reach-item'
		);
		const grow = () => {
			cur.style.width = '18px';
			cur.style.height = '18px';
			curR.style.width = '48px';
			curR.style.height = '48px';
			curR.style.opacity = '.3';
		};
		const shrink = () => {
			cur.style.width = '8px';
			cur.style.height = '8px';
			curR.style.width = '32px';
			curR.style.height = '32px';
			curR.style.opacity = '.6';
		};
		hoverables.forEach((el) => {
			el.addEventListener('mouseenter', grow);
			el.addEventListener('mouseleave', shrink);
		});

		return () => {
			window.removeEventListener('mousemove', onMove);
			cancelAnimationFrame(raf);
		};
	});
</script>

<div id="cur" bind:this={cur}></div>
<div id="cur-r" bind:this={curR}></div>

<style>
	#cur {
		position: fixed;
		width: 8px;
		height: 8px;
		background: var(--gold);
		border-radius: 50%;
		pointer-events: none;
		z-index: 9999;
		transform: translate(-50%, -50%);
		transition:
			width 0.25s,
			height 0.25s;
		mix-blend-mode: multiply;
	}
	#cur-r {
		position: fixed;
		width: 32px;
		height: 32px;
		border: 1.5px solid var(--gold);
		border-radius: 50%;
		pointer-events: none;
		z-index: 9998;
		transform: translate(-50%, -50%);
		transition: all 0.15s;
		opacity: 0.6;
	}
</style>
