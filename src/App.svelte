<script>
	import Color from './Color.svelte'
	import SmallColor from './SmallColor.svelte'
	const paletteOnePrimary = ["#044E54", "#0A6C74", "#0E7C86", "#14919B", "#2CB1BC", "#38BEC9", "#54D1DB", "#87EAF2", "#BEF8FD", "#E0FCFF"]
	const paletteOneNeutrals = ["#102A43", "#243B53", "#334E68", "#486581", "#627D98", "#829AB1", "#9FB3C8", "#BCCCDC", "#D9E2EC", "#F0F4F8"]
	const paletteOneSupportingOne = ["#19216C", "#2D3A8C", "#35469C", "#4055A8", "#4C63B6", "#647ACB", "#7B93DB", "#98AEEB", "#BED0F7", "#E0E8F9"]
	const paletteOneSupportingTwo = ["#5C0B33", "#781244", "#9B1B5A", "#AD2167", "#C42D78", "#DA4A91", "#E668A7", "#F191C1", "#FAB8D9", "#FFE0F0"]
</script>

<main>
	Palette 1
	<div>
		<h3>Primary</h3>
		<h4>Cyan</h4>
		<div class="grid">
			{#each paletteOnePrimary as color}
				<Color {color} />
			{/each}
		</div>
		<h3>Neutrals</h3>
		<h4>Blue Grey</h4>
		<div class="grid">
			{#each paletteOneNeutrals as color}
				<Color {color} />
			{/each}
		</div>
		<h3>Supporting</h3>
		<h4>Indigo</h4>
		<div class="grid-small">
			{#each paletteOneSupportingOne as color}
				<SmallColor {color} />
			{/each}
		</div>
		<h4>Pink</h4>
		<div class="grid-small">
			{#each paletteOneSupportingTwo as color}
				<SmallColor {color} />
			{/each}
		</div>
	</div>
</main>

<style>
	.grid {
		display: grid;
		grid-template-columns: repeat(5, 1fr);
	}
	.grid-small {
		display: grid;
		grid-template-columns: repeat(2, 200px);
	}
</style>