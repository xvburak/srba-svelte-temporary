<script>
	// import {
	// 	onMount
	// } from 'svelte';
	// import axios from 'axios'

	import Carousel from 'svelte-carousel'
	import Color from './Color.svelte'
	// import Image from './Image.svelte'
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

<Carousel autoplay autoplayDuration={2000} arrows={false} dots={false}>
	<Color color="#CDB191" />
	<Color color="#687D45" />
	<Color color="#85B2D3" />
	<!-- <Image url="https://images.unsplash.com/photo-1628258102957-1b77367c8c6c?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=2550&q=80" />
	<Image url="https://images.unsplash.com/photo-1628270680011-41792b21de87?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=2551&q=80" />
	<Image url="https://images.unsplash.com/photo-1577799076422-d258221d6633?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=2555&q=80" /> -->
	<!-- {#each photos as photo}
	<Image url="{photo.url}"/>
	{/each} -->
</Carousel>
<Footer></Footer>

<!-- {/if} -->

<style lang="postcss" global>
	@tailwind base;
	@tailwind components;
	@tailwind utilities;
</style>