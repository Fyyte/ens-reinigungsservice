<script lang="ts">
	import Banner from '$lib/components/Banner.svelte';
	import Hero from '$lib/components/Hero.svelte';
</script>

<header>
	<Banner />
	<section class="content center"><Hero /></section>
	<nav>
		<ul>
			<li><a href="/">Startseite</a></li>
			<li><a href="/posts">Dienstleistungen</a></li>
			<li><a href="/aboutus">Über uns</a></li>
			<li><a href="/environment">Umweltschutz</a></li>
			<li><a href="/jobs">Karriere</a></li>
		</ul>
	</nav>
</header>

<style lang="postcss">
	nav {
		padding: var(--size-4) var(--size-content-px);
		background: #f9f9f9; /* Example background color */
		border-top: 1px solid #ddd; /* Top border */
		border-bottom: 1px solid #ddd; /* Bottom border */
		& ul {
			list-style: none;
			padding: 0;
			margin: 0;
			display: flex;
			flex-wrap: wrap;
			justify-content: center;
			gap: var(--size-8);
			& a {
				font-size: var(--scale-1);
				color: var(--color-primary-500);
				font-weight: var(--weight-bold);
				text-decoration: none;
			}
		}
		& > :nth-child(2) {
			/* Specifically target the Hero component for custom styling if needed */
			margin: 0 var(--size-8); /* Adds horizontal margin around the Hero component */
		}
		@media screen and (max-width: 768px) {
			flex-direction: column;
			& ul {
				display: grid;
				grid-template-columns: 1fr;
				gap: var(--size-2);
				justify-items: center;
			}
		}
	}
</style>
