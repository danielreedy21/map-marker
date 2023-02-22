<script>
	import { onMount } from 'svelte';
	import { Loader } from '@googlemaps/js-api-loader';

	let map;

	onMount(() => {
		const loader = new Loader({
			apiKey: 'AIzaSyC4cyPSREETc0xru4HcwURRDkIsmYlsHok',
			version: 'weekly',
			libraries: ['places']
		});

		loader.load().then(() => {
			map = new google.maps.Map(document.getElementById('map'), {
				center: { lat: -34.397, lng: 150.644 },
				zoom: 8
			});
		});
	});
</script>

<p class="text-center">Map goes here!</p>
<div id="map" class="h-screen w-full" />

<style></style>
