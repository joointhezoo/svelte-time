<script>
	import Header from '../components/Header.svelte';
	import Nav from '../components/Nav.svelte';
</script>

<Header />
<main>
  <Nav />
	<div class="content">
		<slot />
	</div>
</main>

<style>
	main {
    display: flex;
    height: calc(100% - 60px);
		margin: 0 auto;
	}
	.content {
		width: 100%;
		margin: 0 24px;
	}
	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>