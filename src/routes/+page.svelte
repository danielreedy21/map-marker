<script>
	import '../app.css';
	let a = 2;
	let b = 4;

	function increaseA() {
		a++;
	}
	function increaseB() {
		b++;
	}
	function decreaseA() {
		a--;
	}
	function decreaseB() {
		b--;
	}
</script>

<header class="flex justify-center">
	<p>{a} + {b} = {a + b}</p>
</header>
<div class="flex flex-row place-content-evenly font-bold">
	<button class="" on:click={increaseA}> Increase A </button>
	<button on:click={increaseB}> Increase B </button>
	<button on:click={decreaseA}> Decrease A </button>
	<button on:click={decreaseB}> Decrease B </button>
</div>

<!-- <Map /> -->
<style lang="postcss">
</style>
