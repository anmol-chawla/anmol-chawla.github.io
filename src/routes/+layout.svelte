<script>
	import '../app.css';

	/**
	 * Map of page name to path
	 *
	 * @type {{name: string, path: string}[]}
	 */
	var locationMap = [
		{ name: 'Home', path: '/' },
		{ name: 'Blog', path: '/blog' },
		{ name: 'Projects', path: '/projects' }
	];
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

<slot />

<style>
	.navigation-bar {
		display: flex;
		align-items: center;
		justify-content: space-around;
	}
</style>
