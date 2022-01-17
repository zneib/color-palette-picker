<script>
	import Color from './Color.svelte'
	import SmallColor from './SmallColor.svelte'
	const paletteOnePrimary = ["#044E54", "#0A6C74", "#0E7C86", "#14919B", "#2CB1BC", "#38BEC9", "#54D1DB", "#87EAF2", "#BEF8FD", "#E0FCFF"]
	const paletteOneNeutrals = ["#102A43", "#243B53", "#334E68", "#486581", "#627D98", "#829AB1", "#9FB3C8", "#BCCCDC", "#D9E2EC", "#F0F4F8"]
	const paletteOneSupportingOne = ["#19216C", "#2D3A8C", "#35469C", "#4055A8", "#4C63B6", "#647ACB", "#7B93DB", "#98AEEB", "#BED0F7", "#E0E8F9"]
	const paletteOneSupportingTwo = ["#5C0B33", "#781244", "#9B1B5A", "#AD2167", "#C42D78", "#DA4A91", "#E668A7", "#F191C1", "#FAB8D9", "#FFE0F0"]
	const paletteOneSupportingThree = ["#610404", "#780A0A", "#911111", "#A61B1B", "#BA2525", "#D64545", "#E66A6A", "#F29B9B", "#FACDCD", "#FFEEEE"]
	const paletteOneSupportingFour = ["#513C06", "#7C5E10", "#A27C1A", "#C99A2E", "#E9B949", "#F7D070", "#F9DA8B", "#F8E3A3", "#FCEFC7", "#FFFAEB"]
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
		<div class="supporting-section">
			<div class="color-wrapper">
				<h4>Indigo</h4>
				<div class="grid-small">
					{#each paletteOneSupportingOne as color}
						<SmallColor {color} />
					{/each}
				</div>
			</div>
			<div class="color-wrapper">
				<h4>Pink</h4>
				<div class="grid-small">
					{#each paletteOneSupportingTwo as color}
						<SmallColor {color} />
					{/each}
				</div>
			</div>
		</div>
		<div class="supporting-section">
			<div class="color-wrapper">
				<h4>Red</h4>
				<div class="grid-small">
					{#each paletteOneSupportingThree as color}
						<SmallColor {color} />
					{/each}
				</div>
			</div>
			<div class="color-wrapper">
				<h4>Yellow</h4>
				<div class="grid-small">
					{#each paletteOneSupportingFour as color}
						<SmallColor {color} />
					{/each}
				</div>
			</div>
		</div>
	</div>
</main>

<style>
	.grid {
		display: grid;
		grid-template-columns: repeat(5, 1fr);
	}
	.grid-small {
		columns: 2;
		column-width: 120px;
	}
	.color-wrapper {
		margin: 0 50px;
	}
	.supporting-section {
		width: 100%;
		display: flex;
		margin-bottom: 20px;
	}
</style>