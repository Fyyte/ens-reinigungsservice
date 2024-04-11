<script>
	export let icon = '';
	export let action = () => {};
</script>

<button class="fab" on:click={action}>
	{#if icon}
		{icon}
	{/if}
	<slot />
</button>

<style>
	.icon {
		margin-right: var(--size-4);
	}
	.fab {
		position: fixed;
		left: 50%;
		bottom: 14px;
		transform: translateX(-50%); /* Center it horizontally */
		background-color: #447991;
		color: white;
		border: none;
		padding: 12px 24px;
		border-radius: 28px; /* Adjust based on your design preference */
		box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
		display: flex;
		justify-content: center;
		align-items: center;
		cursor: pointer;
		transition: background-color 0.3s;
		font: var(--text-lg); /* Adjust based on your design preference */
		width: auto;
		height: 60px;
		z-index: 1000;

		@media screen and (max-width: 768px) {
			transform: translateX(-83%);
			height: auto;
		}
	}
	.fab:hover {
		background-color: #447991;
	}
	.fab:focus {
		outline: none;
	}

	.fab img {
		margin-right: 8px; /* Space between icon and label */
		height: 24px; /* Adjust based on your design preference */
		width: 24px; /* Adjust based on your design preference */
	}
</style>
