<script>
	import { onMount } from 'svelte';
	import { Loader } from '@googlemaps/js-api-loader';

	let map;

	// let markers = [
	// 	{
	// 		position: new google.maps.LatLng(41.99, 87.65)
	// 	}
	// ];

	onMount(() => {
		const loader = new Loader({
			apiKey: import.meta.env.VITE_GOOGLEAPIKEY,
			version: 'weekly',
			libraries: ['places']
		});

		loader.load().then(() => {
			map = new google.maps.Map(document.getElementById('map'), {
				center: { lat: 41.9989, lng: -87.6583 },
				zoom: 8
			});
		});
	});
</script>

<!-- <p class="text-center">Map goes here!</p> -->
<div id="map" class="h-screen w-full" />

<style></style>
