<script>
  import { onMount } from 'svelte'

  export let color
  export let color2

  let card

  onMount(() => {
    var c = card.childNodes;
    if (color && !color2) {
      c[2].style.backgroundColor = color
    } 
    if (color && color2) {
      c[2].style.backgroundImage = `linear-gradient(to right bottom, ${color}, ${color2})`
    } 
  })
</script>

<style lang="scss">
  @import '../scss/components/card';
</style>

<div class="card" bind:this={card}>
  <div class="card__side card__side--front">
    <slot name="front"/>
  </div>
  <div class="card__side card__side--back">
    <slot name="back" />
  </div>
</div>