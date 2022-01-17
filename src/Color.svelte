<script>
  export let color = ''
</script>

<div class="large-color">
  <button class="grid-color" style="background-color: {color}" on:click={navigator.clipboard.writeText(color)}></button>
  <p>{color}</p>
</div>

<style>
  .large-color {
    transition: .3s;
  }
  @media(max-width: 1286px) {
		.large-color {
			margin-right: 10px;
		}
	}
  .large-color:hover {
    transform: scale(1.2);
  }
  .grid-color {
    width: 130px;
    height: 50px;
    outline: none;
    border: none;
    margin: 10px 0 0 0;
    cursor: pointer;
  }
  p {
    margin: 8px 0 0 0;
    font-size: 10px;
  }
</style>