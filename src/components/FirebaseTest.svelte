<!-- using this to test how to connent the application to Firebase -->
<script>
	// import firebaseConfig from '../lib/firebaseConfig.js';
	import { auth } from '../lib/firebase/firebase.client';
	import { GoogleAuthProvider, signInWithPopup } from 'firebase/auth';
	import { onMount } from 'svelte';

	onMount(() => {});

	function googleSignUp() {
		const provider = new GoogleAuthProvider();
		signInWithPopup(auth, provider)
			.then((result) => {
				// This gives you a Google Access Token. You can use it to access the Google API.
				const credential = GoogleAuthProvider.credentialFromResult(result);
				const token = credential.accessToken;
				// The signed-in user info.
				const user = result.user;
				// IdP data available using getAdditionalUserInfo(result)
				// ...
			})
			.catch((error) => {
				// Handle Errors here.
				const errorCode = error.code;
				const errorMessage = error.message;
				// The email of the user's account used.
				const email = error.customData.email;
				// The AuthCredential type that was used.
				const credential = GoogleAuthProvider.credentialFromError(error);
				// ...
			});
	}
</script>

<div class="bg-green-100 cursor-pointer" on:click={googleSignUp} on:keydown={() => {}}>
	Sign in With Google!
</div>
