<script>
  import { onMount } from 'svelte';
  import Nav from '$lib/components/Nav.svelte';
</script>

<Nav />
<div class="wrapper">
  <br /><br />
  <div class="head">
    <h1>What's that all about</h1>
  </div>
  <div class="container">
    <div class="one">
      <h2>Why Ewingar Rising?</h2>
      <br />
      <p>
        Some stuff about fires and or floods and how the people of Ewingar get
        together to something and something
      </p>
    </div>
    <div class="two">
      <h2>What Now?</h2>
      <br />
      <p>
        Some stuff about this years event honouring the many changes since the
        2019 bushfires and all the community and resiliance and blah blah blah
      </p>
    </div>
    <div class="three">
      <h2>What For?</h2>
      <br />
      <p>
        Some stuff about paying artists and where raised funds go and how
        splendid well cut grass is.
      </p>
    </div>
    <div class="four">
      <h2>Who Done What?</h2>
      <br />
      <p>
        Some stuff about organisations who made this possible and who did the
        mowing and other stuff.
      </p>
    </div>
  </div>
  <div class="foot">
    <div class="logo1">logo1</div>
    <div class="logo2">logo2</div>
    <div class="logo3">logo3</div>
    <div class="logo4">logo4</div>
    <div class="logo5">logo5</div>
  </div>
</div>

<style lang="scss" src="../../lib/scss/pages/_about.scss">
</style>
