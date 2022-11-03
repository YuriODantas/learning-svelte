<script lang="ts">
    import Botao from "./Botao.svelte";
    import Linha from "./Linha.svelte";
    import Tela from "./Tela.svelte";

    let valor = '0'

    let numeroDigitado = (numero: string) => {
      valor += numero
    }

</script>

<div class="calculadora">
  <Tela valor={valor} />
  <Linha>
    <Botao destaque triplo texto="AC" onClick={numeroDigitado} />
    <Botao operacao texto="/" onClick={numeroDigitado} />
  </Linha>
  <Linha>
    <Botao texto="7" onClick={numeroDigitado} />
    <Botao texto="8" onClick={numeroDigitado} />
    <Botao texto="9" onClick={numeroDigitado} />
    <Botao operacao texto="*" onClick={numeroDigitado}/>
  </Linha>
  <Linha>
    <Botao texto="4" onClick={numeroDigitado} />
    <Botao texto="5" onClick={numeroDigitado} />
    <Botao texto="6" onClick={numeroDigitado} />
    <Botao operacao texto="+" onClick={numeroDigitado} />
  </Linha>
  <Linha>
    <Botao texto="1" onClick={numeroDigitado} />
    <Botao texto="2" onClick={numeroDigitado} />
    <Botao texto="3" onClick={numeroDigitado} />
    <Botao operacao texto="-" onClick={numeroDigitado} />
  </Linha>
  <Linha>
    <Botao duplo texto="0" onClick={numeroDigitado} />
    <Botao texto="," onClick={numeroDigitado} />
    <Botao destaque texto="=" onClick={numeroDigitado} />
  </Linha>
</div>

<style>
  .calculadora {
    background-color: var(--cor-fundo);
    height: 220px;
    width: 150px;
    padding: 10px;
    border-radius: 10px;

    display: flex;
    flex-direction: column;
  }
</style>