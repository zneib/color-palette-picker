<script>
  export let color = ''
</script>

<div class="small-color">
  <button class="grid-color" style="background-color: {color}" on:click={navigator.clipboard.writeText(color)}>
  </button>
  <p>{color}</p>
</div>

<style>
  .small-color {
    display: flex;
    align-items: center;
  }
  .grid-color {
    width: 32px;
    height: 32px;
    outline: none;
    border: none;
    margin: 10px 0 0 0;
    cursor: pointer;
  }
  p {
    margin-left: 5px;
    font-size: 10px;
  }
</style>