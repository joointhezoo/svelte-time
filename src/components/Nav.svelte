<script>
	import {isActive, url} from '@sveltech/routify'

	const links = [
    ['./routify', 'routify'],
    ['./loading', 'Loading animation'],
    ['./lifecycle', 'Lifecycle'],
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
		padding: 0;
    border-right: 1px solid #dadada;
    box-shadow: #dadada80 4px 0 14px;
	}
	li {
    padding: 12px 24px;
		border-bottom: 1px solid #ddd;
		list-style: none;
	}
	a {
		font-weight: 300;
		font-size: 16px;
		color: #333;
	}
	.selected {
		font-weight: 500;
		letter-spacing: -0.38px;
	}
</style>