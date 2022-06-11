<!-- 
	@component
	Sample slide/carousel component with Svelte Splide
	@link https://github.com/Splidejs/svelte-splide
	@link https://splidejs.com/guides/options
 -->
<script lang="ts">
	import { Splide, SplideSlide } from "@splidejs/svelte-splide";
	import "@splidejs/svelte-splide/css";

	export let images: {
		src: string;
		alt?: string;
	}[] = [];
</script>

<Splide
	options={{ rewind: true, heightRatio: 0.5 }}
	aria-label="Astro Svelte Splide example"
	class="my-svelte-splide"
>
	{#each images as item}
		<SplideSlide>
			<img class="object-cover" src={item.src} alt={item.alt || ""} />
		</SplideSlide>
	{/each}
</Splide>

<style>
	:global(.my-svelte-splide .splide__slide) {
		background: #000;
	}
</style>
