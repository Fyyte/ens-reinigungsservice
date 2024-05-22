<script>
	import Card from './Card.svelte';

	export let post;
</script>

<Card href={`/post/${post.slug}`} data-sveltekit-prefetch>
	<slot slot="title">{post.title}</slot>
	<div slot="thumbnail">
		{@html post.preview.html}
	</div>
	<div slot="content">
		{#each post.headings.slice(0, -1) as heading}
			<li>{heading.value}</li>
		{/each}
	</div>
</Card>

<style>
	li {
		list-style-type: square;
		white-space: nowrap;
		overflow: hidden;
		text-overflow: ellipsis;
	}
</style>
