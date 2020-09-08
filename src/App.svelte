<script>
	export let name;
	import Header from './components/Header.svelte';
</script>
<main>
    <Header />
    <content>
        <h1>Hello {name}!</h1>
        <p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
    </content>
</main>

<style>
	main {
		margin: 0 auto;
	}
    content {
        width: 100%;
        text-align: center;
    }
	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>