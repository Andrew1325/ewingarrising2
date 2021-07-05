<script>
  export let images = []
</script>

<style lang="scss">
  @import '../scss/components/composition';
</style>

<div class="composition">
{#each images as image, i}
  <img src={image.img} alt={image.name} class="{`composition__photo composition__photo--p${i+1}`}">
{/each}
</div>