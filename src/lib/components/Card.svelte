<script>
	export let as = 'div';
	export let href = undefined;

	let _class = undefined;
	export { _class as class };
</script>

<svelte:element this={as} class={[_class].join(' ')}>
	<a {href} data-sveltekit-prefetch>
		{#if $$slots.title}
			<div class="title">
				<slot name="title" />
			</div>
		{/if}

		{#if $$slots.thumbnail}
			<div class="img">
				<slot name="thumbnail" />
			</div>
		{/if}

		<!-- 		{#if $$slots.content}
			<div class="content">
				<slot name="content" />
			</div>
		{/if} -->
	</a>
</svelte:element>

<style>
	.title {
		font-size: 1.2em;
		margin-bottom: var(--size-2);
		color: var(--color-primary);
		font-weight: bold;
		text-align: center;
	}

	.content {
		overflow: hidden;
		text-overflow: ellipsis; /* Improved handling for overflow text */
		white-space: nowrap; /* Adjust to avoid unnecessary wrapping */
		font: var(--text-xs);
		padding: var(--size-2);
		min-height: 220px;
		width: 100%;
	}

	.img img {
		width: 100%;
		height: auto; /* Changed to maintain image aspect ratio */
		object-fit: cover;
	}

	.img {
		height: 150px; /* Adjusted height */
		overflow: hidden;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	a {
		display: flex;
		flex-direction: column;
		justify-content: space-between; /* Adjust space distribution */
		height: auto; /* Changed to auto to accommodate varying content sizes */
		text-decoration: none;
		color: inherit;
		background: #f9f9f9;
		border: 1px solid #ddd;
		padding: var(--size-4);
		border-radius: var(--size-2);
		transition: transform 0.3s ease; /* Smooth scale transition */
	}

	a:hover {
		transform: scale(1.01);
	}
</style>
