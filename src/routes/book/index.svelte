<script>
  import Nav from '$lib/components/Nav.svelte';
  import Button from '$lib/components/Button.svelte';
  import EBLoader from '$lib/components/EBLoader.svelte';

  function exampleCallback() {
    console.log('checked out');
  }

  function onLoaded() {
    window.EBWidgets.createWidget({
      widgetType: 'checkout',
      eventId: '155495377861',
      modal: true,
      modalTriggerElementId: 'eventbrite-widget-modal-trigger-155495377861',
      onOrderComplete: exampleCallback,
    });
  }

  // var exampleCallback = function () {
  //   console.log('Order complete!');
  // };

  let show = false;

  // onMount(() => {
  //   setTimeout(() => {
  //     window.EBWidgets.createWidget({
  //       widgetType: 'checkout',
  //       eventId: '155495377861',
  //       modal: true,
  //       modalTriggerElementId: 'eventbrite-widget-modal-trigger-155495377861',
  //       onOrderComplete: exampleCallback,
  //     });
  //     show = true;
  //   }, 5000);
  // });
</script>

<!-- <svelte:head>
  <script
    src="https://www.eventbrite.com.au/static/widgets/eb_widgets.js"></script>
</svelte:head> -->

<EBLoader
  url="https://www.eventbrite.com.au/static/widgets/eb_widgets.js"
  on:loaded={onLoaded}
/>
<Nav />

Book

<button
  class="button--holder"
  id="eventbrite-widget-modal-trigger-155495377861"
>
  Book Now
</button>

<style src="../../lib/scss/pages/_book.scss"></style>
