<!-- 
	@component
	Sample slide/carousel component with Svelte Splide
	@link https://github.com/Splidejs/svelte-splide
	@link https://splidejs.com/guides/options
 -->
<script>
	import { Splide, SplideSlide } from "@splidejs/svelte-splide";
	import "@splidejs/svelte-splide/css";

	const img1Src =
		"https://images.unsplash.com/photo-1653450283266-c788c2ca4ab2?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=800";
	const img2Src =
		"https://images.unsplash.com/photo-1649330944677-427f4e9d3c4d?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=800";
</script>

<Splide
	options={{ rewind: true, heightRatio: 0.5 }}
	aria-label="Astro Svelte Splide example"
	class="my-svelte-splide"
>
	<SplideSlide>
		<img class="object-cover" src={img1Src} alt="" />
	</SplideSlide>
	<SplideSlide>
		<img class="object-cover" src={img2Src} alt="" />
	</SplideSlide>
</Splide>

<style>
	:global(.my-svelte-splide .splide__slide) {
		background: #000;
	}
</style>
