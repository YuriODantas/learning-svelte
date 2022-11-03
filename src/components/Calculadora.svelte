<script lang="ts">
    import Botao from "./Botao.svelte";

</script>

<div class="calculadora">
  <Botao texto="7"/>
  <Botao texto="8"/>
  <Botao texto="9"/>
</div>

<style>
  .calculadora {
    height: 220px;
    width: 150px;
    background-color: var(--cor-fundo);
    display: flex;
    flex-direction: column;
  }
</style>