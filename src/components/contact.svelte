<script>
	let name = '',
		email = '',
		subject = '',
		message = '';
	let sent = false;

	function sendMsg() {
		sent = true;
		// Wire up to your backend / form service here
	}
</script>

<section id="contact">
	<div class="contact-inner">
		<div class="contact-left">
			<div class="section-tag light">Connect</div>
			<h2 class="section-h light">Let's Start a<br /><em>Conversation.</em></h2>
			<p class="contact-p">
				Whether you are a financial institution, conference organiser, journalist, fellow
				practitioner, or entrepreneur — the conversation starts here.
			</p>
			<div class="c-links">
				<a href="mailto:iamjerryosagie@gmail.com" class="c-link">
					<div class="c-link-icon">✉</div>
					 iamjerryosagie@gmail.com
				</a>
				<a
					href="https://www.linkedin.com/in/jerry-osagie-84708323"
					target="_blank"
					rel="noopener"
					class="c-link"
				>
					<div class="c-link-icon" style="font-size:.75rem;font-weight:700;">in</div>
					 linkedin.com/in/jerry-osagie
				</a>
				<a href="#" class="c-link">
					<div class="c-link-icon">📍</div>
					 Lagos, Nigeria
				</a>
				<a href="https://jerryosagie.co" class="c-link">
					<div class="c-link-icon">🌐</div>
					 jerryosagie.co
				</a>
			</div>
		</div>

		<div class="contact-form">
			<div class="form-h">Send a Message</div>
			<div class="fg-row">
				<div class="fg"><input type="text" placeholder="Your name" bind:value={name} /></div>
				<div class="fg"><input type="email" placeholder="Email address" bind:value={email} /></div>
			</div>
			<div class="fg">
				<input
					type="text"
					placeholder="Subject — speaking, advisory, media, partnership..."
					bind:value={subject}
				/>
			</div>
			<div class="fg">
				<textarea placeholder="Your message..." bind:value={message}></textarea>
			</div>
			<button class="f-btn" on:click={sendMsg}>Send Message →</button>
			{#if sent}
				<div class="f-ok">✓ Message received — I'll be in touch soon.</div>
			{/if}
		</div>
	</div>
</section>

<style>
	#contact {
		background: var(--navy);
		padding: 9rem 6vw 7rem;
	}
	.contact-inner {
		max-width: 1200px;
		margin: 0 auto;
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 7rem;
		align-items: start;
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
	.contact-p {
		font-size: 0.98rem;
		font-weight: 300;
		color: rgba(255, 255, 255, 0.5);
		line-height: 1.85;
		margin-top: 1.5rem;
		margin-bottom: 3rem;
	}
	.c-links {
		display: flex;
		flex-direction: column;
		gap: 0.8rem;
	}
	.c-link {
		display: flex;
		align-items: center;
		gap: 1rem;
		text-decoration: none;
		color: rgba(255, 255, 255, 0.7);
		font-size: 0.92rem;
		padding-bottom: 0.8rem;
		border-bottom: 1px solid rgba(196, 137, 58, 0.1);
		transition: color 0.2s;
	}
	.c-link:last-child {
		border-bottom: none;
	}
	.c-link:hover {
		color: var(--gold2);
	}
	.c-link-icon {
		width: 34px;
		height: 34px;
		border-radius: 4px;
		background: rgba(196, 137, 58, 0.1);
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 0.85rem;
		flex-shrink: 0;
	}
	.contact-form {
		background: rgba(255, 255, 255, 0.04);
		border: 1px solid rgba(196, 137, 58, 0.15);
		border-radius: 6px;
		padding: 2.5rem;
	}
	.form-h {
		font-family: var(--serif);
		font-size: 1.4rem;
		font-weight: 600;
		color: #fff;
		margin-bottom: 1.8rem;
	}
	.fg {
		margin-bottom: 1.1rem;
	}
	.fg input,
	.fg textarea {
		width: 100%;
		background: rgba(255, 255, 255, 0.05);
		border: 1px solid rgba(196, 137, 58, 0.18);
		border-radius: 3px;
		padding: 0.8rem 1rem;
		color: #fff;
		font-size: 0.88rem;
		outline: none;
		transition: border-color 0.2s;
	}
	.fg input::placeholder,
	.fg textarea::placeholder {
		color: rgba(255, 255, 255, 0.28);
	}
	.fg input:focus,
	.fg textarea:focus {
		border-color: var(--gold);
	}
	.fg textarea {
		min-height: 110px;
		resize: vertical;
	}
	.fg-row {
		display: grid;
		grid-template-columns: 1fr 1fr;
		gap: 1rem;
	}
	.f-btn {
		width: 100%;
		background: var(--gold);
		color: var(--navy);
		border: none;
		padding: 0.95rem;
		border-radius: 3px;
		font-size: 0.78rem;
		font-weight: 700;
		letter-spacing: 0.12em;
		text-transform: uppercase;
		cursor: pointer;
		transition:
			background 0.2s,
			transform 0.2s;
	}
	.f-btn:hover {
		background: var(--gold2);
		transform: translateY(-2px);
	}
	.f-ok {
		margin-top: 1rem;
		color: var(--gold2);
		font-size: 0.85rem;
		text-align: center;
	}
	@media (max-width: 1000px) {
		.contact-inner {
			grid-template-columns: 1fr;
			gap: 3rem;
		}
	}
</style>
