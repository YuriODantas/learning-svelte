<script lang="ts">
    import Botao from "./components/Botao.svelte";
</script>

<main>
	<Botao texto="7" />
	<Botao texto="8" />
	<Botao texto="9" />
</main>

<style>
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
</style>