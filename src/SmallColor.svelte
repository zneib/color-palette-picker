<script>
  export let color = ''
</script>

<div>
  <button class="grid-color" style="background-color: {color}" on:click={navigator.clipboard.writeText(color)}></button>
  <p>{color}</p>
</div>

<style>
  .grid-color {
    width: 32px;
    height: 32px;
    outline: none;
    border: none;
    margin: 10px 0 0 0;
    cursor: pointer;
  }
  p {
    margin: 0;
  }
</style>