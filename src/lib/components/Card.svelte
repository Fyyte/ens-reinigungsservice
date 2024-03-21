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
		<div class="footer">
			<slot name="eyebrow" />
		</div>
	</a>
</svelte:element>

<style>
	.img:hover {
		-webkit-transform: scale(1.01);
		transform: scale(1.01);
	}
	.title {
		text-align: center;
		font-weight: bold;
		text-decoration: underline;
	}
	a {
		text-decoration: none;
		color: inherit;
	}
</style>
