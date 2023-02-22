<script>
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

<header class="text-red-700 flex justify-center">
	<p>{a} + {b} = {a + b}</p>
</header>

<div class="flex flex-row place-content-evenly font-bold">
	<button
		class="text-black
	rounded-md border-4 border-black 
	px-4 bg-sky-700 drop-shadow-2xl
	hover:shadow-lg shadow-black"
		on:click={increaseA}
	>
		Increase A
	</button>

	<button
		class="text-black
	rounded-md border-4 border-black 
	px-4 bg-sky-700 drop-shadow-2xl
	hover:shadow-lg shadow-black"
		on:click={increaseB}
	>
		Increase B
	</button>

	<button
		class="text-black
	rounded-md border-4 border-black 
	px-4 bg-sky-700 
	hover:shadow-lg shadow-black"
		on:click={decreaseA}
	>
		Decrease A
	</button>

	<button
		class="text-black
	rounded-md border-4 border-black 
	px-4 bg-sky-700 drop-shadow-2xl
	hover:shadow-lg shadow-black"
		on:click={decreaseB}
	>
		Decrease B
	</button>
</div>
