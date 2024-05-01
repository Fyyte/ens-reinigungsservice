<script>
	import PostPreview from '$lib/components/PostPreview.svelte';
	import PostDate from '$lib/components/PostDate.svelte';

	export let posts;
</script>

<div class="container">
	{#each posts as post}
		<article class="post-grid">
			<PostPreview {post}>
				<!-- 			<slot slot="eyebrow">
					<PostDate {post} />
				</slot> -->
			</PostPreview>
		</article>
	{/each}
</div>

<style>
	.container {
		display: grid;
		grid-template-columns: repeat(auto-fill, minmax(350px, 1fr));
		gap: 1rem;
	}

	.post-grid {
		display: flex;
		flex-direction: column;
	}
</style>
