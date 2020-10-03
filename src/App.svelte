<script>
	import Intro from "./Intro.svelte";

	export let name;
</script>

<style>
	.top-bar {
		display: flex;
		margin: 1em 5em 5em 5em;
		align-items: center;
		flex-wrap: wrap;
		justify-content: space-between;
	}

	.top-bar .title {
		font-family: "Yesteryear", cursive;
		font-size: 42px;
		background: -webkit-linear-gradient(90deg, #ff8d4d, #f4494e);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
	}

	.top-bar .nav {
		text-decoration: none;
		font-family: "Roboto", sans-serif;
		padding-right: 40px;
		color: #6e6d7a;
		font-size: 18px;
		font-weight: 600;
	}
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}

	content {
		padding: 1em;
		margin: auto;
	}
</style>

<svelte:head>
	<link
		href="https://fonts.googleapis.com/css2?family=Yesteryear&display=swap"
		rel="stylesheet" />
	<link
		href="https://fonts.googleapis.com/css2?family=Roboto&display=swap"
		rel="stylesheet" />
</svelte:head>

<div class="top-bar">
	<a href="/" class="title">Groovy Design Studios</a>
	<div>
		<a href="#about" class="nav">About</a>
		<a href="#services" class="nav">Services</a>
		<a href="#pricing" class="nav">Pricing</a>
		<a href="#contact" class="nav">Contact</a>
	</div>
</div>
<content>
	<Intro />
	<main>
		<h1>Hello {name}!</h1>
		<p>
			Visit the
			<a href="https://svelte.dev/tutorial">Svelte tutorial</a>
			to learn how to build Svelte apps.
		</p>
	</main>
</content>
