<script>
  export let size = 60;
  export let color = "#ff3e00";
  let unit = "px";
</script>

<style>
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
</style>

<div class="circle" style="--size: {size}{unit}; --color: {color}; --borderWidth: {size/8}{unit}"></div>
