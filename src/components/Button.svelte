<script lang="ts">
  export let text: string = ''
  export let double: boolean = false
  export let triple: boolean = false
  export let operation: boolean = false
  export let highlight: boolean = false

  export let onClick: (value: string) => void = () => {}
</script>

<button 
  on:click={() => onClick(text)}
  class="button" 
  class:triple 
  class:double
  class:operation
  class:highlight
>
  {text}
</button>

<style>
  .button {
    margin: 0;
    border: 1px solid var(--background-color);
    flex-basis: 25%;
  }

  .double {
    flex-basis: 50%;
  }

  .triple {
    flex-basis: 75%;
  }
  
  .operation {
    background-color: #ffa600;
    color: #FFF;
  }
  
  .highlight {
    background-color: #ff0000;
    color: #FFF;
  }
</style>