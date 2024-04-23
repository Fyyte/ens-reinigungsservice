<script lang="ts">
	export let productInfo = {
		name: 'ENS Reinigungsservice',
		description: 'einfach nur sauber'
	};
	import logo from '$lib/assets/logo.webp';
</script>

<section class="content center">
	<header class="header">
		<div class="logo-wrapper">
			<a href="/"><img class="logo" src={logo} alt=" Icon" /></a>
		</div>
		<div class="app__infos">
			<a href="/"><h1 class="name supertitle">{productInfo.name}</h1></a>
			<a href="/"><p class="description">{productInfo.description}</p></a>
		</div>
	</header>
</section>

<style lang="postcss">
	section {
		background-image: url('$lib/assets/hero_bg.webp');
		background-size: cover;
	}
	.header {
		background-color: var(--color-gray-50);
		box-shadow: 0px 0px 10px 0px rgba(0, 0, 0, 0.45) inset;
		//backdrop-filter: blur(10px);
		border-radius: 10px;
		padding: var(--size-4);
		display: -ms-flexbox;
		display: flex;
		-ms-flex-direction: row;
		flex-direction: row;
		margin-bottom: 16px;
		-ms-flex-align: center;
		align-items: center;
		font: var(--text-sm);

		& h1 {
			color: var(--color-primary);
		}

		@media (max-width: 768px) {
			margin-top: 32px;
			margin-bottom: 16px;
		}
	}

	.logo-wrapper {
		display: inline-block;
		background-size: contain;
		max-width: 64px;
		max-height: 64px;
		margin-right: var(--size-4);
		width: 100%;
		height: 100%;
		background-repeat: no-repeat;
	}

	.logo {
		border-radius: 10.5%;
		-webkit-mask-size: cover;
		mask-size: cover;
		width: 100%;
		height: auto;
	}

	.name {
		margin: 0;
		@media (max-width: 768px) {
			font-size: var(--text-sm);
		}
	}

	a {
		text-decoration: none;
	}

	.description {
		font: var(--text-lg);
		color: var(--color-primary-0);
		font-weight: bold;
	}
</style>
