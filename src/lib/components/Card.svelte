<script>
	export let as = 'div';
	export let href = undefined;

	let _class = undefined;
	export { _class as class };
</script>

<svelte:element this={as} class={[_class].join(' ')}>
	<a {href} data-sveltekit-prefetch>
		{#if $$slots.description}
			<div class="img">
				<slot name="description" />
			</div>
		{/if}

		{#if $$slots.title}
			<div class="title">
				{#if href}
					<slot name="title" />
				{:else}
					<slot name="title" />
				{/if}
			</div>
		{/if}
	</a>
</svelte:element>

<style>
	.background-image .img {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		object-fit: cover;
		z-index: 1;
		transition: transform 0.3s ease;
	}

	.overlay {
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		bottom: 0;
		background-color: rgba(0, 0, 0, 0.5);
		z-index: 2;
	}

	.title {
		position: absolute;
		width: 100%;
		bottom: 10%;
		left: 0;
		text-align: center;
		font-weight: bold;
		z-index: 3;
		color: var(--color-primary);
		background-color: var(--color-gray-50);
	}

	a {
		display: block;
		height: 100%;
		text-decoration: none;
		color: inherit;
		position: relative;
	}

	a:hover {
		-webkit-transform: scale(1.01);
		transform: scale(1.01);
	}
</style>
