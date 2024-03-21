<script>
	import PostsList from '$lib/components/PostsList.svelte';

	/** @type {import('./$types').PageData} */
	export let data;

	$: isFirstPage = data.page === 1;
	$: hasNextPage = data.posts[data.posts.length - 1]?.previous;
</script>

<section class="content">
	<div class="text-cards">
		<article>
			<h2>Für ein makellos sauberes Büro</h2>
			<p>
				E.N.S bietet umfassende Büroreinigung in Wien, gewährleistet durch unser Team von
				Reinigungsexperten. Wir legen Wert auf umweltschonende Mittel und maßgeschneiderte Lösungen,
				die sich nach Ihren Bedürfnissen richten, um das Wohlbefinden Ihrer Kunden und Mitarbeiter
				zu fördern.
			</p>
		</article>
		<article>
			<h2>Professionelle Pflege für Ihren Arbeitsplatz</h2>
			<p>
				Unser Angebot umfasst Teppich-, Möbel- und Parkettbodenreinigung mit größter Sorgfalt, um
				den Wert Ihrer Ausstattung zu erhalten. Wir bieten Ihnen eine kosteneffiziente Lösung für
				eine professionelle Büroumgebung.
			</p>
		</article>
		<article>
			<h2>Ihr Komplettservice für Büroreinigung in Wien</h2>
			<p>
				Von der Teppichreinigung bis zur Entrümpelung - unser umfassender Service deckt alle Aspekte
				der Büroreinigung ab. Flexibilität und Streben nach höchster Qualität garantieren Ihre
				Zufriedenheit.
			</p>
		</article>
	</div>

	<h1>Unsere Dienstleistungen</h1>

	<div class="posts-section">
		<PostsList posts={data.posts} />
	</div>
</section>

<style>
	.content {
		font: var(--text-lg);
	}

	h1 {
		margin-block: var(--size-8);
		color: var(--color-primary);
		font-weight: bold;
	}

	h2 {
		margin-block: var(--size-4);
		color: var(--color-primary);
		font-weight: bold;
	}

	.text-cards {
		display: flex;
		flex-wrap: wrap;
		gap: var(--size-4);
		margin: 0;
		padding: 0;
	}

	.text-cards article {
		background: #f9f9f9;
		border: 1px solid #ddd;
		padding: var(--size-4);
		border-radius: var(--size-2);
		flex-grow: 1;
		flex-basis: calc(50% - var(--size-2)); /* Adjust basis for gap */
	}

	@media only screen and (max-width: 600px) {
		.text-cards {
			flex-direction: column;
		}

		.text-cards article {
			flex-basis: 100%;
		}
	}
</style>
