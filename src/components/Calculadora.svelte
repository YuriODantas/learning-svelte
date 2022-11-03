<script lang="ts">
    import Botao from "./Botao.svelte";
    import Linha from "./Linha.svelte";

</script>

<div class="calculadora">
  <Linha>
    <Botao triplo texto="AC"/>
    <Botao texto="/"/>
  </Linha>
  <Linha>
    <Botao texto="7"/>
    <Botao texto="8"/>
    <Botao texto="9"/>
    <Botao texto="*"/>
  </Linha>
  <Linha>
    <Botao texto="4"/>
    <Botao texto="5"/>
    <Botao texto="6"/>
    <Botao texto="+"/>
  </Linha>
  <Linha>
    <Botao texto="1"/>
    <Botao texto="2"/>
    <Botao texto="3"/>
    <Botao texto="-"/>
  </Linha>
  <Linha>
    <Botao duplo texto="0"/>
    <Botao texto=","/>
    <Botao texto="="/>
  </Linha>
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