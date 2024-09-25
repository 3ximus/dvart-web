<script>
	import '../app.css';
	import vlogo from '$lib/images/vlogo.png';
</script>

<div class="app">
	<header>
		<img src={vlogo} alt="V" />
	</header>

	<main>
		<slot />
	</main>

	<footer>
		<p>Footer</p>
	</footer>
</div>

<style scoped>
	header {
		background-color: var(--color-bg-0);
		width: 100%;
		position: sticky;
		display: flex;
		justify-content: center;
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
		padding: 12px;
	}
</style>
