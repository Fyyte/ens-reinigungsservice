<script>
	import PostsList from '$lib/components/PostsList.svelte';

	/** @type {import('./$types').PageData} */
	export let data;

	$: isFirstPage = data.page === 1;
	$: hasNextPage = data.posts[data.posts.length - 1]?.previous;
</script>

<section class="content">
	<ul class="text-cards">
		<li>
			<p>
				<strong>Tailored to Your Needs</strong> Recognizing the uniqueness of every business, customized
				web solutions are designed to meet specific requirements. An online presence should mirror the
				brand identity and goals, ensuring it precisely represents what the business stands for.
			</p>
		</li>
		<li>
			<p>
				<strong>Engage Your Audience Everywhere</strong> Websites and applications adapt seamlessly to
				any device, whether it be desktops, tablets, or smartphones. Providing a consistent and enjoyable
				user experience across all platforms is essential for engaging and retaining the audience.
			</p>
		</li>
		<li>
			<p>
				<strong>Expertise and Support</strong> The journey to success is a partnership, with a team of
				experts offering guidance and support at every step. From the initial concept to launch and beyond,
				ensuring the success of projects with experienced insights and assistance.
			</p>
		</li>
		<li>
			<p>
				<strong>Transparent and Affordable Pricing</strong>
				Top-notch web solutions are accessible without a hefty price tag. A commitment to transparent
				and affordable pricing options guarantees no compromise on quality. Outstanding value for the
				investment allows for an online presence to flourish, all while keeping the budget intact.
			</p>
		</li>
	</ul>

	<h1>Blog Posts</h1>

	<div class="posts-section">
		<PostsList posts={data.posts} />
	</div>

	<!-- pagination -->
	<div class="pagination">
		{#if !isFirstPage}
			<a href={`/posts/${data.page - 1}`} data-sveltekit-prefetch class="link">Previous</a>
		{:else}
			<div />
		{/if}

		{#if hasNextPage}
			<a href={`/posts/${data.page + 1}`} data-sveltekit-prefetch class="link">Next</a>
		{/if}
	</div>
</section>

<style>
	.content {
		font: var(--text-lg);
	}
	h1 {
		margin-block: var(--size-6);
	}

	.pagination {
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding-top: 4rem; /* pt-16 */
		padding-bottom: 2rem; /* pb-8 */
	}

	.link {
		display: flex;
		align-items: center;
		gap: 0.5rem;
		font-weight: 500;
		color: #3b82f6;
	}

	.text-cards {
		display: grid;
		grid-template-columns: repeat(2, 1fr); /* Two columns by default */
		gap: var(--size-12);
		margin: 0;
		padding: 0;
		list-style: none;
	}

	.text-cards li {
		/*  border: 1px solid #ddd;  */
		border-radius: var(--size-2);
	}

	.text-cards li strong {
		display: block;
		font-size: 1.2em; /* Larger font size for the title */
		margin-bottom: var(--size-2); /* Space below the title */
		color: var(--color-primary); /* Title color */
	}

	@media only screen and (max-width: 600px) {
		.text-cards {
			grid-template-columns: 1fr; /* One column on mobile */
		}
	}
</style>
