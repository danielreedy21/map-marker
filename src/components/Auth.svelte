<script>
	let register = false;
	let email = '';
	let password = '';
	let confirmPassword = '';
</script>

<div class="flex flex-col items-center justify-center">
	<h1>{register ? 'Sign Up' : 'Sign In'}</h1>

	<form action="" class="flex flex-col">
		<label>
			<input bind:value={email} type="text" placeholder="Email" />
		</label>

		<label>
			<input bind:value={password} type="text" placeholder="Password" />
		</label>

		{#if register}
			<label>
				<input bind:value={confirmPassword} type="password" placeholder="Confirm Password" />
			</label>
		{/if}

		<button class="bg-gray-500">Submit</button>
	</form>

	{#if register}
		<div
			class="cursor-pointer"
			on:click={() => {
				register = false;
			}}
			on:keydown={() => {}}
		>
			Already have an account?
			<p class="bg-gray-400">Log in</p>
		</div>
	{:else}
		<div
			class="cursor-pointer"
			on:click={() => {
				register = true;
			}}
			on:keydown={() => {}}
		>
			Don't have an account?
			<p class="bg-gray-400">Sign Up</p>
		</div>
	{/if}
</div>
