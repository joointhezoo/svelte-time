<script>
    import { onMount, onDestroy } from 'svelte';
    import Loading  from '../components/Loading.svelte';

    let timer;
    let loaded = false;

    onMount(async () => {
        timer = setTimeout(() => {
            loaded = true;
        }, 1000)
    });

    onDestroy(() => {
        console.log('🎉 destroy succeed');
        clearTimeout(timer);
    });

</script>

<style>
    .photos {
        width: 100%;
        display: flex;
        flex-wrap: wrap;
    }

    figure {
        width: 33%;
        display: flex;
        flex-wrap: wrap;
        margin: 4px 0;
    }

    kbd {
        background: #efefef;
        text-transform: none;
    }

    h1 {
        color: #ff3e00;
        text-transform: uppercase;
        font-size: 4em;
        font-weight: 100;
    }

</style>

<h1>Lifecycle<br/>(<kbd>onMount</kbd>/<kbd>onDestroy</kbd>)</h1>
<p><kbd>onMount</kbd>, which runs after the component is first rendered to the DOM.</p>
<p>when you leave this page,<kbd>onDestroy</kbd> will destroy setTimeout function, which is used in <kbd>onMount</kbd></p>
<p><i>Check the console log when you leave this page 🤗</i></p>
<div class="photos">
	{#if loaded}
      <h2>🎉 Loading succeed</h2>
	{:else}
      <Loading />
	{/if}
</div>