<!-- <script>
	import jobs from '$lib/assets/jobs.png';
</script> -->

<section class="content">
	<h1>Werden Sie Teil unseres Teams</h1>
	<p>
		Bei ENS Reinigungsservice e.U. wächst unser Kundenstamm stetig, und um diesen wachsenden
		Anforderungen gerecht zu werden, sind wir auf der Suche nach zuverlässigen und engagierten
		Mitarbeitern. Uns ist es wichtig, dass unser Team nicht nur aus Fachkräften besteht, sondern
		auch aus Menschen, die mit Leidenschaft bei der Sache sind.
	</p>
	<p>
		Wir bieten eine faire Bezahlung, ein motivierendes Arbeitsumfeld und den direkten Kontakt zu
		Kunden, die Ihre Arbeit zu schätzen wissen. Unsere Vision ist es, dass jeder Mitarbeiter mit
		einem Lächeln zur Arbeit kommt und dieses auch am Ende des Tages noch trägt. Dafür setzen wir
		auf ein Team, das nicht nur fachlich kompetent ist, sondern auch Wert auf ein gepflegtes
		Erscheinungsbild legt.
	</p>
	<p>
		Wenn Sie Erfahrung in der Reinigungsbranche haben und Teil eines Unternehmens werden möchten,
		das Wert auf Qualität, Mitarbeiterzufriedenheit und Umweltschutz legt, dann freuen wir uns
		darauf, Sie kennenzulernen. Einzelheiten zu offenen Positionen und dem Bewerbungsverfahren
		besprechen wir gerne in einem persönlichen Gespräch.
	</p>
	<p>Sind Sie bereit, mit einem Lächeln zu uns zu stoßen? Wir freuen uns auf Ihre Bewerbung!</p>
</section>

<style lang="postcss">
	.images {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: var(--size-4);

		& img {
			border: 1px solid #ddd; /* Example border */
			border-radius: var(--size-2);
		}

		& img:hover {
			-webkit-transform: scale(1.01);
			transform: scale(1.01);
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
