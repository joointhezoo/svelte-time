<script>
	import {isActive, url} from '@sveltech/routify'

	const links =
			[
				['/', 'Home'],
				['./about', 'About'],
			]
</script>

<ul>
	{#each links as [path, name]}
		<li>
			<a href={$url(path)} class:selected={$isActive(path)}>{name}</a>
		</li>
	{/each}
</ul>

<style>
	ul {
	    box-sizing: border-box;
	    height: 100%;
	    min-width: 240px;
	    margin: 0;
	    padding: 24px 0;
	    border-right: 1px solid #dadada;
	    box-shadow: #dadada80 4px 0 14px;
	}
	li {
	    margin: 4px 24px;
	}
	.selected {
		text-decoration: underline;
	}
</style>