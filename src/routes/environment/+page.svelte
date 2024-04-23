<script>
	import picnic from '$lib/assets/picnic.webp';
	import trash from '$lib/assets/trash.webp';
	import nature from '$lib/assets/nature.webp';
</script>

<section class="content">
	<div class="head">
		<div>
			<h1>Unser Engagement für den Umweltschutz</h1>
			<h2>Verantwortungsvolle Reinigung für eine grünere Zukunft</h2>
		</div>
		<img
			src={nature}
			alt="Forest"
			width="350px"
			style="display: block; margin: auto;padding-top:1rem"
		/>
	</div>
	<p>
		Bei ENS Reinigungsservice e.U. ist uns bewusst, dass unsere Geschäftsaktivitäten Hand in Hand
		mit der Verantwortung für die Umwelt gehen. Unser Ziel ist es, nicht nur saubere und hygienische
		Räumlichkeiten zu schaffen, sondern auch unseren Teil zum Schutz unseres Planeten beizutragen.
		Wir glauben fest daran, dass jeder Schritt hin zu mehr Nachhaltigkeit zählt.
	</p>

	<h2>Unsere umweltfreundlichen Praktiken:</h2>
	<ul class="text-cards">
		<li class="text-box">
			<p>
				<strong>Einsatz umweltfreundlicher Reinigungsmittel</strong> Wir wählen unsere Reinigungsprodukte
				sorgfältig aus und bevorzugen Lösungen, die sowohl effektiv als auch umweltverträglich sind.
				Dies bedeutet den Verzicht auf harte Chemikalien zugunsten von Produkten mit natürlichen und
				biologisch abbaubaren Inhaltsstoffen.
			</p>
		</li>
		<li class="text-box">
			<p>
				<strong>Wassersparende Reinigungstechniken</strong> Wasser ist eine kostbare Ressource, und wir
				setzen innovative Reinigungsmethoden ein, die den Wasserverbrauch minimieren. Durch effiziente
				Techniken und Geräte streben wir danach, unseren ökologischen Fußabdruck zu reduzieren.
			</p>
		</li>
		<li>
			<img src={trash} alt="recycling" />
		</li>
		<li>
			<img src={picnic} alt="picnic" />
		</li>
		<li class="text-box">
			<p>
				<strong>Recycling und Abfallmanagement</strong> Wir legen großen Wert auf die Reduzierung von
				Abfällen und fördern aktives Recycling sowohl intern als auch bei unseren Kunden. Unser Ziel
				ist es, das Bewusstsein für die Wichtigkeit von Recycling zu schärfen und praktische Lösungen
				für die Mülltrennung anzubieten.
			</p>
		</li>
		<li class="text-box">
			<p>
				<strong>Bildung und Sensibilisierung</strong> Ein wichtiger Teil unseres Engagements ist die
				Aufklärung unseres Teams und unserer Kunden über Umweltschutzpraktiken. Durch regelmäßige Schulungen
				und Informationsmaterialien fördern wir ein tiefgreifendes Verständnis für die Bedeutung nachhaltiger
				Reinigung.
			</p>
		</li>
	</ul>

	<div>
		<p>
			Unser Engagement für den Umweltschutz ist ein wesentlicher Bestandteil unserer
			Unternehmensphilosophie. Wir sind stolz darauf, in jedem Aspekt unserer Arbeit proaktiv zu
			sein und kontinuierlich nach neuen Wegen zu suchen, um unseren Beitrag zum Schutz der Umwelt
			zu leisten.
		</p>
		<p>
			<strong
				>Entdecken Sie, wie ENS Reinigungsservice e.U. den Unterschied macht – für saubere Räume und
				eine saubere Umwelt.</strong
			>
		</p>
	</div>
</section>

<style lang="postcss">
	.head {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: var(--size-4);

		& img {
			border: none;
		}

		& img:hover {
			-webkit-transform: scale(1.03);
			transform: scale(1.03);
		}
		@media screen and (max-width: 768px) {
			grid-template-columns: 1fr;
		}
	}
	img {
		border: 1px solid #ddd; /* Example border */
		border-radius: var(--size-2);
	}
	img:hover {
		-webkit-transform: scale(1.01);
		transform: scale(1.01);
	}

	strong {
		color: var(--color-primary);
	}
	p {
		margin-block: var(--size-12);
		padding: var(--size-4);
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

	.text-box {
		background: #f9f9f9; /* Example background color */
		border: 1px solid #ddd; /* Example border */
		border-radius: var(--size-2);
	}

	.text-cards li strong {
		display: block;
		font-size: 1.2em; /* Larger font size for the title */
		margin-bottom: var(--size-2); /* Space below the title */
		color: var(--color-primary); /* Title color */
	}
</style>
