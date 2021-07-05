<script lang="ts">
  import { onMount } from 'svelte';

  export let minor = false;
  export let href = null;
  export let outline = false;
  export let color = null;
  export let line = false;
  export let square = false;
  export let rounded = false;
  export let textColor = null;
  export let disabled = false;

  let btn;

  onMount(() => {
    var c = btn.childNodes;
    c[0].style.lineHeight = '1';
    if (color) {
      if (outline) {
        c[0].style.backgroundColor = 'rgba(0,0,0,0)';
        c[0].style.border = `1px solid ${color}`;
      } else {
        c[0].style.backgroundColor = color;
      }
      if (textColor) {
        c[0].style.color = `${textColor}`;
      }
      if (square) {
        c[0].style.borderRadius = '0px';
        rounded = false;
      }
      if (line) {
        c[0].style.outline = `1px solid ${color}`;
        c[0].style.outlineOffset = '2px';
      }
    } else if (outline && color === null) {
      c[0].style.backgroundColor = 'rgba(0,0,0,0)';
      c[0].style.border = '1px solid #fff';
      if (textColor) {
        c[0].style.color = `${textColor}`;
      }
    }
  });
</script>

<div bind:this={btn}>
  {#if minor}
    <a href="#" class="btn-text">
      <slot />
    </a>
  {:else}
    <a
      id="button"
      {href}
      class={rounded
        ? 'btn btn--round btn--white btn--animated'
        : 'btn btn--white btn--animated'}
      on:click
      {disabled}
    >
      <slot />
    </a>
  {/if}
</div>

<style lang="scss" src="../scss/components/_button.scss">
</style>
