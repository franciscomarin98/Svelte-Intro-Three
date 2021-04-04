<script>
	import Data from "./Data.svelte";

	export let name,
		lastName = "Marin";
	let myObject = {
		propiedadOne: "Nickname",
		propiedadTwo: "Sisco",
	};
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>
		My name is {name}
		{lastName}
	</p>
	<Data {...myObject} />
</main>
