<script lang="ts">
  import Button from '$lib/components/Button.svelte';
  import Nav from '$lib/components/Nav.svelte';
  import Artists from '$lib/components/HomeArtists.svelte';

  import { onMount } from 'svelte';

  let loaded = false;

  onMount(() => {
    setTimeout(() => {
      loaded = true;
    }, 2000);
  });
</script>

{#if !loaded}
  <div class="things--holder">
    <div class="things">
      <div class="thing even">
        <div class="thing odd">
          <div class="thing even">
            <div class="thing odd">
              <div class="thing even">
                <div class="thing odd">
                  <div class="thing even">
                    <div class="thing odd" />
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
{:else}
  <Nav />
  <div class="container y-scroll y-mandatory">
    <div class="wrapper">
      <div class="element">
        <div class="main--content" id="main" style="margin-top:0px;">
          <div class="main--content_logo">
            <img src="./phoenixDevice.svg" alt="phoenix logo" />
          </div>
          <br />
          <div class="line--holder">
            <div class="line" />
          </div>
          <div class="main--content_body">
            <div id="welcome">
              <small>Fundraising Music Festival</small><br />
              <h1>Ewingar Rising</h1>
              <small>September 17 - 19 2021</small>
            </div>
            <br /><br />
            <p id="scroll">
              Scroll down to find out why we're doing this and which great
              artists will be playing
            </p>
            <br /><br />
            <div id="book">
              <small>I know enough, just let me...</small><br /><br />
              <Button href="/book" square line color="#1ab16a" textColor="white"
                >Book Now</Button
              >
            </div>
          </div>
        </div>
      </div>
      <div class="element">
        <div class="second" id="second">
          <div class="second--content">
            <h1>Ewingar Rising. Again</h1>
            <br /><br />
            <p>
              Ewingar Rising fundraising music festival returns to the Northern
              NSW town of Ewingar, two years after the bushfires!
            </p>
            <br /><br />
            <p>
              And this time …. the grass is green, the birds are singing and the
              trees are in recovery from the bushfires of September- November
              2019.
              <br /><br />
              Ewingar Rising 2019 was a three-day fundraising music festival staged
              just six weeks after our area burned.
              <br /><br />
              We’ve invited back the bands who supported us in 2019 – many who had
              gigs cancelled during the pandemic.
              <br /><br />
              And this time…. the bands will be paid, and half of any profit will
              be donated to SupportAct, Australia’s only organisation to deliver
              crisis relief to those in the music industry.
            </p>
          </div>
        </div>
      </div>
      <div class="element">
        <div class="third" id="third">
          <br />
          <div class="spacer" />
          <Artists />
        </div>
      </div>
    </div>
  </div>
{/if}

<style lang="scss" src="../lib/scss/pages/_index.scss">
</style>
