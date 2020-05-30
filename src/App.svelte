<script>
	import Slider from './Slider.svelte'

	export let sliderValA = 0;
	export let sliderValB = 15;
</script>

<main>
	<h1>Simple SvelteJS slider component</h1>

	<p>Slider A value is {sliderValA}</p>
	<Slider bind:value={sliderValA} min="0" max="10" />

	<p>Slider B value is {sliderValB}</p>
	<Slider bind:value={sliderValB} min="0" max="30" />

	<p>A + B is {sliderValA + sliderValB}</p>

	<p>
		This <code>Slider</code> component:
	</p>
	<ul>
		<li>Has custom CSS which makes it easy to manipulate on a touch screen, while still looking simple & similar across platforms. This takes <a href="https://css-tricks.com/styling-cross-browser-compatible-range-inputs-css/">a lot of CSS</a> for a range input.</li>
		<li>Is separate from the main app component, which is nice because it has custom CSS that only has to be written once. (It’s a component.)</li>
		<li>Has props for value, min, & max.</li>
		<li>Works just like a normal, plain-HTML range input does in Svelte. You can <a href="https://svelte.dev/tutorial/numeric-inputs">easily bind its value</a> to the state in the component it is used within.</li>
	</ul>
	<p>Note: this is intended more as a test & open example of how a Slider component can be made in SvelteJS. It is not necessarily representative of best practices or something that you should reuse without testing & improvement.</p>
	<p>Have an idea of how to improve it? Please file an issue or make a pull request in the <a href="https://github.com/arrowtype/svelte-slider">GitHub Repo!</a></p>
</main>

<style>
	main {
		height: 100%;
		display: grid;
		justify-content: center;
		align-content: center;
		line-break: 1.5;
	}

	a {
		text-decoration: underline;
	}
	p, li {
		max-width: 55ch;
		margin-bottom: 1em;
	}
	code {
		font-size: 1.4em;
	}
</style>