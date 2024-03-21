<script lang="ts">
	import logo from '$lib/assets/logo.png';
	import { getAuthContext } from '$lib/auth-context';
	import Hero from '$lib/components/Hero.svelte';
	import { getContext } from 'svelte';
	const user = getAuthContext();
</script>

<header>
	<Hero />
	<nav>
		<ul>
			<li><a href="/">Startseite</a></li>
			<li><a href="/aboutus">Über uns</a></li>
			<li><a href="/environment">Umweltschutz</a></li>
			<li><a href="/jobs">Karriere</a></li>
			<!-- 			<li><a href="/fotos">Fotos</a></li> -->
			<!-- <li><a href="/team">Team</a></li> -->
		</ul>
	</nav>
</header>

<style lang="postcss">
	nav {
		padding: var(--size-4) var(--size-content-px);
		background: #f9f9f9; /* Example background color */
		border-top: 1px solid #ddd; /* Top border */
		border-bottom: 1px solid #ddd; /* Bottom border */
		//border-radius: var(--size-2);
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
	}
</style>
