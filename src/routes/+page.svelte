<script lang="ts">
	import Merch from './Merch.svelte';
	import merchpic1 from '$lib/images/itempic_1.webp';
	import merchpic2 from '$lib/images/itempic_2.webp';
	import merchpic3 from '$lib/images/itempic_3.webp';
	import merchpic4 from '$lib/images/itempic_4.webp';

	let enableMerch = true;
</script>

<section>
	<div class="music-section">
		<iframe
			width="560"
			height="315"
			src="https://www.youtube-nocookie.com/embed/videoseries?si=tidPOaiU-SwIyUhl&amp;controls=0&amp;list=PLJipLc0D7d9ReZYUE4QTzbLtfx6Kxz6yy&autoplay=1&mute=1"
			title="YouTube video player"
			frameborder="0"
			allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
			referrerpolicy="strict-origin-when-cross-origin"
			allowfullscreen
		></iframe>
		<div class="side-text music">MUSIC</div>
	</div>

	{#if enableMerch}
		<div class="merch-section">
			<Merch src={merchpic4}></Merch>
			<Merch src={merchpic3}></Merch>
			<Merch src={merchpic1}></Merch>
			<Merch src={merchpic2}></Merch>
			<div class="side-text merch">MERCH</div>
		</div>
	{/if}
</section>

<style>
	section {
		display: flex;
		justify-content: center;
		flex-direction: column;
		gap: 10px;
	}

	.music-section {
		display: flex;
		justify-content: center;
		align-items: center;
		position: relative;
	}
	.music-section iframe {
		width: 100%;
		border-radius: 2px;
	}

	.merch-section {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: 10px;
		position: relative;
	}

	.side-text {
		position: absolute;
		writing-mode: vertical-rl;
		text-orientation: mixed;
		font-size: 2.5rem;
		color: white;
	}

	.side-text.music {
		right: -44px;
		top: 0;
		margin: 0;
	}

	.side-text.merch {
		left: -50px;
		top: 0;
		margin: 0;
	}
	@media (max-width: 800px) {
		.side-text {
			font-size: 1.3rem;
		}
		.side-text.music {
			right: -26px;
		}

		.side-text.merch {
			left: -28px;
		}
	}
</style>
