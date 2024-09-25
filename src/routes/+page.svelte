<script>
	import Merch from './Merch.svelte';
	import merchpic1 from '$lib/images/itempic_1.jpg';
	import merchpic2 from '$lib/images/itempic_2.jpg';
	import merchpic3 from '$lib/images/itempic_3.jpg';
	import merchpic4 from '$lib/images/itempic_4.jpg';
</script>

<svelte:head>
	<title>Louis Dvart</title>
	<meta name="description" content="Louis Dvart Artist Page" />
</svelte:head>

<section>
	<div class="music-section">
		<iframe
			width="560"
			height="315"
			src="https://www.youtube-nocookie.com/embed/videoseries?si=tidPOaiU-SwIyUhl&amp;controls=0&amp;list=PLJipLc0D7d9ReZYUE4QTzbLtfx6Kxz6yy&autoplay=1"
			title="YouTube video player"
			frameborder="0"
			allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
			referrerpolicy="strict-origin-when-cross-origin"
			allowfullscreen
		></iframe>
		<div class="side-text music">MUSIC</div>
	</div>

	<div class="merch-section">
		<Merch src={merchpic4}></Merch>
		<Merch src={merchpic3}></Merch>
		<Merch src={merchpic1}></Merch>
		<Merch src={merchpic2}></Merch>
		<div class="side-text merch">MERCH</div>
	</div>
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
		right: -46px;
		top: 0;
		margin: 0;
	}

	.side-text.merch {
		left: -50px;
		top: 0;
		margin: 0;
	}
</style>
