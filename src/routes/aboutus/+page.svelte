<script>
	import hero from '$lib/assets/hero.png';
</script>

<section class="content">
	<div class="head">
		<div>
			<h1>Über ENS Reinigungsservice</h1>
			<h2>Wo Qualität und Vertrauen Hand in Hand gehen</h2>
		</div>
		<img
			src={hero}
			alt="Büroreinigung"
			width="350px"
			style="display: block; margin: auto;padding-top:1rem"
		/>
	</div>
	<p>
		ENS Reinigungsservice e.U. steht für herausragende Reinigungsleistungen mit einem persönlichen
		Touch. Wir sind nicht nur ein Unternehmen, sondern eine Familie, die sich durch ihre
		Leidenschaft für Sauberkeit und das Wohl ihrer Kunden auszeichnet. Unsere Mission ist es, Ihnen
		nicht nur saubere Räume, sondern ein reines Wohlbefinden zu garantieren.
	</p>

	<h2>Unsere Mission:</h2>
	<ul class="text-cards">
		<li>
			<p>
				<strong>Exzellenz in der Reinigung</strong> Wir setzen hohe Standards in jedem Aspekt unserer
				Arbeit, von der Auswahl unserer Reinigungsmittel bis hin zur Schulung unseres Personals. Unser
				Ziel ist es, über Ihre Erwartungen hinaus zu reinigen und einen makellosen Raum zu hinterlassen.
			</p>
		</li>
		<li>
			<p>
				<strong>Kundenorientierter Service</strong> Bei ENS Reinigungsservice e.U. steht der Kunde im
				Mittelpunkt. Wir hören zu, passen uns Ihren Bedürfnissen an und stellen sicher, dass jede Dienstleistung
				Ihre individuellen Anforderungen erfüllt.
			</p>
		</li>
		<li>
			<p>
				<strong>Nachhaltigkeit und Umweltbewusstsein</strong> Wir glauben an die Verantwortung gegenüber
				unserer Umwelt und wählen unsere Reinigungsmittel und -methoden entsprechend. Wo immer möglich,
				nutzen wir umweltfreundliche Produkte und Techniken.
			</p>
		</li>
		<li>
			<p>
				<strong>Unser Team</strong> Unser größtes Kapital sind unsere Mitarbeiter. Ein Team aus erfahrenen
				und leidenschaftlichen Reinigungsfachkräften, die sich durch ihre Zuverlässigkeit und Liebe zum
				Detail auszeichnen. Wir sind stolz darauf, ein Umfeld zu fördern, in dem sich jeder einzelne
				Mitarbeiter wertgeschätzt fühlt und exzellente Leistungen erbringen kann.
			</p>
		</li>
	</ul>

	<div>
		<p>
			Wir sind stolz darauf, ein vertrauenswürdiger Partner für unsere Kunden zu sein, indem wir
			konsequent außergewöhnliche Reinigungsdienstleistungen bieten. Unser Ziel ist es, nicht nur
			Räume zu reinigen, sondern auch zur Gesundheit und Zufriedenheit der Menschen beizutragen, die
			diese Räume nutzen.
		</p>
		<p>
			<strong
				>Schließen Sie sich der ENS-Familie an und erleben Sie den Unterschied, den ein
				professioneller Reinigungsservice mit Herz machen kann.</strong
			>
		</p>
	</div>
</section>

<style lang="postcss">
	.head {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: var(--size-4);

		& img:hover {
			-webkit-transform: scale(1.03);
			transform: scale(1.03);
		}
		@media screen and (max-width: 768px) {
			grid-template-columns: 1fr;
		}
	}
	strong {
		color: var(--color-primary);
	}
	p {
		margin-block: var(--size-12);
	}

	.text-cards {
		display: grid;
		grid-template-columns: repeat(2, 1fr); /* Two columns by default */
		gap: var(--size-4);
		margin: 0;
		padding: 0;
		list-style: none;

		@media screen and (max-width: 768px) {
			grid-template-columns: 1fr; /* One column on small screens */
		}
	}

	.text-cards li {
		background: #f9f9f9; /* Example background color */
		border: 1px solid #ddd; /* Example border */
		padding: var(--size-4);
		border-radius: var(--size-2);
	}

	.text-cards li strong {
		display: block;
		font-size: 1.2em; /* Larger font size for the title */
		margin-bottom: var(--size-2); /* Space below the title */
		color: var(--color-primary); /* Title color */
	}
</style>
