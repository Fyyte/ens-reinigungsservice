<script>
	import logo from '$lib/assets/logo_detailed.webp';
	import meister from '$lib/assets/meister.webp';
</script>

<footer>
	<div class="footer-container">
		<div class="footer-contact">
			<p class="bold">ENS Reinigungsservice e.U</p>
			<p>Geschäftsführer: Zoran Andelkovic</p>
			<p>Email: <a href="mailto:office@ens-reinigung.at">office@ens-reinigung.at</a></p>
			<p>Telefon: <a href="tel:+43 676 7898465">+43 676 7898465</a></p>
			<p><strong>Büro Öffnungszeiten:</strong></p>
			<p><strong>Montag</strong> 08:30-16:30</p>
			<p><strong>Dienstag</strong> 11:30-16:30</p>
			<p><strong>Mittwoch</strong> 08:30-16:30</p>
			<p><strong>Donnerstag</strong> 08:30-16:30</p>
			<p><strong>Freitag</strong> 08:30-15:00</p>
		</div>
		<div class="footer-links">
			<p><a href="/privacy">Datenschutz</a></p>
			<p><a href="/legal">Impressum</a></p>
		</div>
		<div class="logo footer-logo">
			<img src={logo} alt="logo" />
			<img src={meister} alt="meister" />
			<p>Made by <a href="https://dinweldik.com" target="_blank">dinweldik.com</a></p>
		</div>
	</div>
</footer>

<style>
	.logo {
		text-align: center;
		& img {
			height: var(--size-32);
			width: var(--size-32);
		}
		& p {
			font: var(--text-xs);
			margin-top: 10px;
		}
		& a {
			color: #ffaaaa;
			text-decoration: none;
		}
	}
	.bold {
		font-weight: bold;
	}
	footer {
		padding: var(--size-10); /* Spacing around the content */
		margin-bottom: var(--size-14);
		@media screen and (max-width: 768px) {
			margin-bottom: var(--size-32);
		}
	}

	.footer-container {
		display: flex;
		justify-content: space-between;
	}

	.footer-contact,
	.footer-logo {
		width: 40%;
	}

	.footer-links {
		width: 20%; /* Each column takes up roughly half the footer */
	}

	.footer-contact h3,
	.footer-links h3 {
		margin-bottom: 20px; /* Spacing below headings */
	}

	.footer-contact p,
	.footer-links p {
		line-height: 1.5; /* Line spacing for readability */
		margin-bottom: 10px; /* Spacing between paragraphs */
	}

	.footer-contact a,
	.footer-links a {
		color: var(--color-primary);
		text-decoration: none; /* No underline for links */
	}

	.footer-contact a:hover,
	.footer-links a:hover {
		text-decoration: underline; /* Underline on hover for links */
	}
	@media (max-width: 768px) {
		.footer-container {
			flex-direction: column;
			align-items: center; /* Centers the children horizontally */
		}
		.footer-contact,
		.footer-links,
		.logo {
			/* Apply full width and centering for all footer children */
			width: 100%; /* Full width on smaller screens */
			margin-bottom: 20px; /* Spacing between sections on smaller screens */
			text-align: center; /* Center the content for contact and links */
		}
		.logo img {
			margin: 0 auto; /* Additional centering specifically for the logo image */
			display: block; /* Ensures that auto margins work for horizontal centering */
		}
	}
</style>
