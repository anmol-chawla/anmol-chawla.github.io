<script>

	/**
	 * Map of page name to path
	 *
	 * @type {{name: string, path: string}[]}
	 */
    export let locationMap;

</script>


<div class="navigation-bar">
	{#each locationMap as { name, path }, index}
		<div>
			<a href={path}>{name}</a>
		</div>
		{#if index + 1 != locationMap.length}
			<div>
				<p>|</p>
			</div>
		{/if}
	{/each}
</div>

<style>
	.navigation-bar {
		display: flex;
		align-items: center;
		justify-content: space-around;
	}
</style>
