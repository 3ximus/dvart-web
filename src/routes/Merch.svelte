<script>
	export let src = '';
</script>

<div class="container">
	<a href="https://ig.me/m/LOUISDVART" target="_blank">
		<img {src} alt="Louis Dvart homekit merch t-shirt" />

		<div class="scrolling-text">
			<div class="scrolling-container">
				<div class="scrolling-container__item">
					sold out, dm for restock&nbsp;&nbsp;&nbsp;<it>"HOMEKIT" by LD</it>&nbsp;&nbsp;&nbsp;
				</div>
				<div class="scrolling-container__item">
					sold out, dm for restock&nbsp;&nbsp;&nbsp;<it>"HOMEKIT" by LD</it>&nbsp;&nbsp;&nbsp;
				</div>
				<div class="scrolling-container__item">
					sold out, dm for restock&nbsp;&nbsp;&nbsp;<it>""HOMEKIT" by LD"</it>&nbsp;&nbsp;&nbsp;
				</div>
			</div>
		</div>
	</a>
</div>

<style>
	div.container {
		position: relative;
	}
	img {
		width: 100%;
		height: 100%;
		border-radius: 2px;
	}

	.scrolling-text {
		position: absolute;
		width: 100%;
		white-space: nowrap;
		overflow: hidden;
		box-sizing: border-box;
		bottom: 20px;
		background-color: yellow;
		color: black;
		font-weight: bold;
		font-size: 1rem;
		padding: 4px;
		padding-top: 6px;
		letter-spacing: 0.03rem;
		filter: drop-shadow(0 0.5rem 1rem #000000aa);
	}
	.scrolling-container {
		display: flex;
		width: 690px; /* should be double the width of the text */
		animation-name: infiniteScroll;
		animation-duration: 5s;
		animation-iteration-count: infinite;
		animation-timing-function: linear;
	}
	.scrolling-container__item {
		white-space: nowrap;
	}
	.scrolling-container__item > it {
		font-style: italic;
	}

	@keyframes infiniteScroll {
		from {
			transform: translateX(0);
		}
		to {
			transform: translateX(-50%);
		}
	}
	@media (max-width: 800px) {
		.scrolling-text {
			font-size: 0.8rem;
			padding: 2px;
			padding-top: 4px;
		}
		.scrolling-container {
			display: flex;
			width: 554px;
		}
	}
</style>
