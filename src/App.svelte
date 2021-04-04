<script>
	//Imports
	import Button from "./Button.svelte";
	import Data from "./Data.svelte";

	//States
	let myObject = {
		propiedadOne: "Nickname",
		propiedadTwo: "Sisco",
	};
	let disabled = true;

	//Props
	export let name,
		lastName = "Marin";

	export let buttonOptions = {
		text: "btnComponent",
		disabled: false,
	};
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>
		My name is {name}
		{lastName}
	</p>
	<a href="https://mipagina.com/{name}">Forma 1</a>
	<a href={`https://mipagina.com/${name}`}>Forma 2</a>
	<Data {...myObject} />
	<!-- {console.log(myObject)}
	{@debug myObject} -->
	<input type="text" />
	<button {disabled}>Click</button>
	<Button {...buttonOptions} />
</main>

<style>
	:global(button) {
		border: 1px solid red;
	}
</style>
