<script>
	let text = "lorem ipsum dolor sit amet";
	let count = 0;

	function handleClick() {
		count++;
		text = "You clicked " + count + " times";
	}
</script>

<div class="About">
	<p>{text}</p>
	<div>
		<button on:click={handleClick}>Click me</button>
	</div>
	<p>Counter {count}</p>
</div>

<style>
	p {
		color: var(--theme-color);
	}
</style>
