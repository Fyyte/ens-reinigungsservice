<script>
	import PostsList from '$lib/components/PostsList.svelte';
	import vacuum from '$lib/assets/vacuum.png';

	/** @type {import('./$types').PageData} */
	export let data;

	$: isFirstPage = data.page === 1;
	$: hasNextPage = data.posts[data.posts.length - 1]?.previous;
</script>

<section class="content">
	<div class="head">
		<div>
			<h1>Für ein makellos sauberes Büro</h1>
			<h2>Büroreinigung in Wien und Niederösterreich</h2>
		</div>
		<img
			src={vacuum}
			alt="Büroreinigung"
			width="350px"
			style="display: block; margin: auto;padding-top:1rem"
		/>
	</div>
	<p>
		ENS bietet umfassende Büroreinigung in Wien und Niederösterreich, gewährleistet durch unser Team
		von Reinigungsexperten. Wir legen Wert auf umweltschonende Mittel und maßgeschneiderte Lösungen,
		die sich nach Ihren Bedürfnissen richten, um das Wohlbefinden Ihrer Kunden und Mitarbeiter zu
		fördern.
	</p>
	<ul class="text-cards">
		<li>
			<strong>Professionelle Pflege für Ihren Arbeitsplatz</strong>
			<p>
				Unser Angebot umfasst Teppich-, Möbel- und Parkettbodenreinigung mit größter Sorgfalt, um
				den Wert Ihrer Ausstattung zu erhalten. Wir bieten Ihnen eine kosteneffiziente Lösung für
				eine professionelle Büroumgebung.
			</p>
		</li>
		<li>
			<strong>Ihr Komplettservice für Büroreinigung in Wien und Niederösterreich</strong>
			<p>
				Von der Teppichreinigung bis zur Entrümpelung - unser umfassender Service deckt alle Aspekte
				der Büroreinigung ab. Flexibilität und Streben nach höchster Qualität garantieren Ihre
				Zufriedenheit.
			</p>
		</li>
	</ul>

	<div class="posts-section">
		<h1>Unsere Dienstleistungen</h1>
		<PostsList posts={data.posts} />
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

	.posts-section {
		display: flex;
		flex-direction: column;
		gap: var(--size-12);
		margin-top: var(--size-12);
	}
</style>
