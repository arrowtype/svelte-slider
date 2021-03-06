<script>

	// import slider components
	import Slider from './Slider.svelte'
	import SimpleSlider from './SimpleSlider.svelte'

	// set default slider values here
	export let sliderValA = 0;
	export let sliderValB = 10;
	export let sliderValC = 0;
</script>

<main>
	<h1>A simple SvelteJS slider component</h1>

	<p>Slider A value is {sliderValA}</p>
	<Slider bind:value={sliderValA} min="0" max="10" step="1"/>

	<p>Slider B value is {sliderValB}</p>
	<Slider bind:value={sliderValB} min="0" max="20" step="5"/>

	<p>A + B is {sliderValA + sliderValB}</p>

	<h3>An even simpler slider</h3>

	<p>Slider C value is {sliderValC}</p>

	<SimpleSlider bind:value={sliderValC} min="0" max="30" step="1"/>

	<p>A + B + C is {sliderValA + sliderValB + sliderValC}</p>

	<h2>Description</h2>

	<p>
		This <code>Slider</code> component:
	</p>
	<ul>
		<li>Has custom CSS which makes it easy to manipulate on a touch screen, while still looking simple & similar across platforms. This takes <a href="https://css-tricks.com/styling-cross-browser-compatible-range-inputs-css/">a lot of CSS</a> for a range input.</li>
		<li>Is separate from the main app component, which is nice because it has custom CSS that only has to be written once. (It’s a component.)</li>
		<li>Has props for value, min, & max. It also spreads in additional props you might wish to pass in, such as step.</li>
		<li>Works just like a normal, plain-HTML range input does in Svelte. You can <a href="https://svelte.dev/tutorial/numeric-inputs">easily bind its value</a> to the state in the component it is used within.</li>
	</ul>

	<footer>

		<p><b>Note:</b> this is intended mostly as a test & shared example of how a Slider component can be made in SvelteJS. It is not necessarily representative of best practices in Svelte, and it is probably not something that you should reuse without testing & improvement.</p>

		<p>Thanks to Stack Overflow user @Gh05d for <a href="https://stackoverflow.com/a/62102844/3704306">good advice</a> on simplifying this component.</p>

		<p>Want to see/use this code? Check out the <a href="https://github.com/arrowtype/svelte-slider">GitHub repo!</a> Have an idea of how to improve this? Issues & pull requests welcome.</p>

		<p>Made by <a href="https://arrowtype.com">@ArrowType</a></p>
	</footer>
</main>

<style>
	main {
		margin: 0 auto;
		max-width: 55ch;
		padding: 5vmin 0.5rem;
		line-height: 1.5;
	}
	h1 {
		margin-bottom: 3rem;
	}
	h2 {
		margin-top: 4rem;
	}
	p, li {
		max-width: 55ch;
		margin-bottom: 1em;
	}
	a {
		text-decoration: underline;
		color: currentColor;
	}
	code {
		font-size: 1.4em;
	}
	footer {
		margin-top: 4rem;
		color: #666;
	}
</style>