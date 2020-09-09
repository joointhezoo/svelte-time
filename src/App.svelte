<script>
	import Header from './components/Header.svelte';
	import SideNav from './components/SideNav.svelte';
	import Index from './pages/Index.svelte';
</script>
<Header />
<main>
    <SideNav />
	<Index name={'john doe'}/>
</main>

<style>
	main {
	    display: flex;
	    height: calc(100% - 60px);
		margin: 0 auto;
	}
	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>