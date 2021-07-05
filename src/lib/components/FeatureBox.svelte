<script>
  export let icon = null
</script>

<style lang="scss">
  @import '../scss/components/feature-box';
</style>

<div class="feature-box">
  <i class="{`feature-box__icon ${icon}`}"></i>
  <h3 class="heading-tertiary"><slot name="title"/></h3>
  <p class="feature-box__text">
    <slot/>
  </p>
</div>