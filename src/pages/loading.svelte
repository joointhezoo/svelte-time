<script>
  let size = 60;
  let color = "#ff3e00";
  let unit = "px";
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

  .circle {
    height: var(--size);
    width: var(--size);
    border: var(--borderWidth) solid var(--color);
    border-top-color: transparent;
    border-radius: var(--size);
    animation: rotate 1s linear 0s infinite;
  }

  @keyframes rotate {
    0% {
      transform: rotate(0);
    }
    100% {
      transform: rotate(360deg);
    }
  }
  .setting {
    padding: 24px;
    border-top: 1px solid #ddd;
    min-height: 20%;
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
    <div class="circle" style="--size: {size}{unit}; --color: {color}; --borderWidth: {size/8}{unit}"></div>
  </div>
  <div class="setting">
    <label>size(px)</label>
    <input bind:value={size}/><br/>
    <label>color</label>
    <input bind:value={color}/><br/>
  </div>
</div>
