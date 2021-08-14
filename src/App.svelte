<script>
	// import {
	// 	onMount
	// } from 'svelte';
	// import axios from 'axios'
	
	import Carousel from 'svelte-carousel'
	import Color from './Color.svelte'
	import Image from './Image.svelte'
	import Footer from './Footer.svelte'
	import Header from './Header.svelte'


	// let photos = [];
	// let error = null

	// onMount(async () => {
	// 	try {
	// 		const res = await axios.get('https://jsonplaceholder.typicode.com/photos?_limit=5');
	// 		photos = res.data;
	// 		console.log(photos)
	// 	} catch (e) {
	// 		error = e
	// 	}
	// });

</script>

<!-- {#if error !== null}
  {error}
{:else} -->
<Header></Header>
<Footer></Footer>
<Carousel let:loaded  autoplay autoplayDuration={2000} arrows={false} dots={false}>
	<Image url="/images/foto-1.jpg" />
	<Image url="/images/foto-2.jpg" />
	<Image url="/images/foto-3.jpg" />
	<Image url="/images/foto-4.jpg" />
	
	<!-- {#each photos as photo}
	<Image url="{photo.url}"/>
	{/each} -->
</Carousel>


<!-- {/if} -->

<style lang="postcss" global>
	@tailwind base;
	@tailwind components;
	@tailwind utilities;
</style>