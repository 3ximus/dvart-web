<script>
	import '../app.css';
	import vlogo from '$lib/images/vlogo.png';

	import iglogo from '$lib/images/iglogo.png';
	import ytlogo from '$lib/images/ytlogo.png';
	import spotilogo from '$lib/images/spotilogo.png';
	import tiktoklogo from '$lib/images/tiktoklogo.png';
	import aplmlogo from '$lib/images/aplmlogo.png';
</script>

<div class="app">
	<header>
		<img src={vlogo} alt="V" />
	</header>

	<main>
		<slot />
	</main>

	<footer>
		<h3>FIND V ONLINE</h3>
		<div>
			<a href="https://www.instagram.com/louisdvart/">
				<img src={iglogo} alt="instagram" />
			</a>
			<a href="https://www.youtube.com/@LOUISDVART/">
				<img src={ytlogo} alt="youtube" />
			</a>
			<a href="https://open.spotify.com/intl-pt/artist/1TL1qQoaFtWUt2D85hCOIl">
				<img src={spotilogo} alt="spotify" />
			</a>
			<img src={tiktoklogo} alt="tiktok" />
			<a
				href="https://music.apple.com/pt/artist/louis-dvart/1460848509?at=1l3vpUI&ct=LFV_0ce5b4118ff7ec49af11fe5824a4bf5d&itsct=catchall_p1&itscg=30440&ls=1"
			>
				<img src={aplmlogo} alt="apple" />
			</a>
		</div>
	</footer>
</div>

<style scoped>
	header {
		background-color: var(--color-bg);
		width: 100%;
		position: fixed;
		display: flex;
		justify-content: center;
		z-index: 10;
	}
	header img {
		width: 300px;
		padding: 40px;
	}

	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		padding-top: 140px;
		width: 100%;
		max-width: 50rem;
		margin: 0 auto;
		box-sizing: border-box;
	}

	footer {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 20px;
		padding-bottom: 50px;
	}
	footer div {
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 20px;
	}
	footer a {
		display: flex;
		justify-content: center;
		align-items: center;
	}
	footer img {
		width: 30px;
	}

	@media (max-width: 800px) {
		main {
			max-width: 20rem;
			padding-top: 68px;
		}
		header img {
			width: 150px;
			padding: 20px;
		}
		footer h3 {
			font-size: 1rem;
			margin: 5px;
		}
	}
</style>
