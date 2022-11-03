<script lang="ts">
  export let texto: string = ''
  export let duplo: boolean = false
  export let triplo: boolean = false
  export let operacao: boolean = false
  export let destaque: boolean = false

  export let onClick: (valor: string) => void = () => {}
</script>

<button 
  on:click={() => onClick(texto)}
  class="botao" 
  class:triplo 
  class:duplo
  class:operacao
  class:destaque
>
  {texto}
</button>

<style>
  .botao {
    margin: 0;
    border: 1px solid var(--cor-fundo);
    flex-basis: 25%;
  }

  .duplo {
    flex-basis: 50%;
  }

  .triplo {
    flex-basis: 75%;
  }
  
  .operacao {
    background-color: #ffa600;
    color: #FFF;
  }
  
  .destaque {
    background-color: #ff0000;
    color: #FFF;
  }
</style>