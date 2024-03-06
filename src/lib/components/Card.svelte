<script>
	export let as = 'div';
	export let href = undefined;

	let _class = undefined;
	export { _class as class };
</script>

<svelte:element this={as} class={[_class].join(' ')}>
	{#if $$slots.description}
		<div class="img">
			<slot name="description" />
		</div>
	{/if}

	{#if $$slots.title}
		<div class="title">
			{#if href}
				<div />
				<a {href} data-sveltekit-prefetch>
					<span>
						<slot name="title" />
					</span>
				</a>
			{:else}
				<slot name="title" />
			{/if}
		</div>
	{/if}
	<div class="footer">
		<slot name="eyebrow" />
	</div>
</svelte:element>

<style>
</style>
