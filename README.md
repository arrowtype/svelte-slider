# Simple SvelteJS slider component

To use SvelteJS, please see the [SvelteJS Documentation](https://svelte.dev/).

---

This `Slider` component:

- Has custom CSS which makes it easy to manipulate on a touch screen, while still looking simple & similar across platforms. This takes [a lot of CSS](https://css-tricks.com/styling-cross-browser-compatible-range-inputs-css/) for a range input.
- Is separate from the main app component, which is nice because it has custom CSS that only has to be written once. (It’s a component.)
- Has props for value, min, & max. It also spreads in additional props you might wish to pass in, such as step.
- Works just like a normal, plain-HTML range input does in Svelte. You can [easily bind its value](https://svelte.dev/tutorial/numeric-inputs) to the state in the component it is used within.

**Note:** this is intended mostly as a test & shared example of how a Slider component can be made in SvelteJS. It is not necessarily representative of best practices in Svelte, and it is probably not something that you should reuse without testing & improvement.

Thanks to Stack Overflow user @Gh05d for [good advice](https://stackoverflow.com/a/62102844/3704306) on simplifying this component.

Have an idea of how to improve it? Please file an issue or make a pull request in the GitHub Repo!
