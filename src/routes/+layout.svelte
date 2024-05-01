<script lang="ts">
	import '@fontsource-variable/montserrat';
	import { navigating } from '$app/stores';
	import Footer from './Footer.svelte';
	import Header from './Header.svelte';
	import '$lib/style/app.css';
	import Spinner from '$lib/components/Spinner.svelte';
	import Fab from '$lib/components/Fab.svelte';
	export let data;
</script>

<Fab>
	<p class="noMobile">
		<a href="tel:+436767898465"
			>Jetzt <strong>maßgeschneidertes</strong> und <strong>unverbindliches</strong> Angebot machen lassen!
			📞</a
		>
	</p>

	<p class="mobile">
		<a href="tel:+436767898465">Jetzt anrufen 📞</a>
	</p>
</Fab>

<main>
	<Header />
	{#if $navigating}
		<div class="spinner">
			<Spinner />
		</div>
	{:else}
		<slot />
	{/if}
	<Footer />
</main>

<style lang="postcss">
	.noMobile {
		@media (max-width: 768px) {
			display: none;
		}
	}

	.mobile {
		display: none;
		@media (max-width: 768px) {
			display: block;
		}
	}
	a {
		text-decoration: none;
	}
	main {
		margin: 0;
	}
	.spinner {
		margin-top: var(--size-8);
		display: grid;
		place-items: center;
	}
</style>
