<script>
	import About from "./components/About.svelte";
	import Person from "./components/Person.svelte";
	import Text from "./components/Text.svelte";
	let title = "Hello World";
	let svelteLogo = "https://arepa.s3.amazonaws.com/svelte-logo.png";

	const data = {
		name: "Rod",
		lastName: "Garcia",
		age: 25,
		job: "Developer",
	};
</script>

<main>
	<h1>{title}</h1>
	<About />
	<Text />
	<Person {...data} />
	<div class="svelte-logo-container">
		<img src={svelteLogo} alt="" srcset="" />
	</div>
</main>

<style>
	:global(body) {
		margin: 0;
		padding: 0;
		font-family: sans-serif;
		background-color: #f2eee2;
		color: #0084f6;
	}

	:global(:root) {
		--theme-color: purple;
	}

	.svelte-logo-container {
		width: 500px;
		height: 500px;
	}

	.svelte-logo-container img {
		width: 100%;
		height: auto;
	}
</style>
