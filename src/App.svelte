<script>
	import { onMount } from 'svelte';
	import axios from 'axios'

	import Carousel from 'svelte-carousel'
	import Color from './Color.svelte'
	import Image from './Image.svelte'
	import Footer from './Footer.svelte'
	import Header from './Header.svelte'


	let photos = [];
	let error = null

	onMount(async () => {
		try {
			const res = await axios.get('https://jsonplaceholder.typicode.com/photos?_limit=5');
			photos = res.data;
			console.log(photos)
		} catch (e) {
			error = e
		}
	});
</script>

{#if error !== null}
  {error}
{:else}
<Header></Header>

<Carousel let:loaded autoplay autoplayDuration={2000} arrows={false} dots={false}>
	<Color color="#FF6600"/>
	<Color color="#0066FF"/>
	<Image url="https://a0.muscache.com/im/pictures/prohost-api/Hosting-49190145/original/25df8112-4010-478b-b926-2a47144d668b.jpeg?im_w=720" />
	{#each photos as photo}
	<Image url="{photo.url}"/>
	{/each}
</Carousel>
<Footer></Footer> 

{/if}

<style lang="postcss" global>
	@tailwind base;
	@tailwind components;
	@tailwind utilities;

</style>