<script>
	import Loading from '../components/Loading.svelte';
	let size = 60;
	let color = "#ff3e00";
</script>

<style>
  h1 {
    color: #ff3e00;
    text-transform: uppercase;
    font-size: 4em;
    font-weight: 100;
  }

  .content {
    display: flex;
    flex-direction: column;
    height: 100%;
  }

  .loading {
    display: flex;
    flex: 1;
    align-items: center;
    justify-content: center;
  }

  label {
    display: inline-block;;
    width: 100px;
    text-align: center;
    box-shadow: inset 0 -6px 0 #40b3ff50;
  }
</style>

<div class="content">
  <h1>try change size & color</h1>
  <div class="loading">
      <Loading size={size} color={color}/>
  </div>
  <div class="setting">
    <label>size(px)</label>
    <input bind:value={size}/><br/>
    <label>color</label>
    <input bind:value={color}/><br/>
  </div>
</div>
