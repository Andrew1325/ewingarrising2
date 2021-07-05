<script>
  import Button from '$lib/components/Button.svelte';
  import { onMount } from 'svelte';

  let opac = 0;
  $: arrowOpac = opac;

  let dialog = false;
  let image;
  let bio;
  let name;

  let descs = [
    'Tex perkins punched some cunt out',
    'Cate McQuillen, creator of dirtgirlworld has agreed to MC Ewingar Rising on Saturday & Sunday AND dirtgirl herself will be hanging out at Kids Corner on Sunday!! A bit about Cate: From Toronto to New York, London to Cannes, Whiporie to Ewingar and right across the Nation, this Emmy Award-winning bush dwelling Filmmaker is passionate about stories that inspire change. On stage she was subtle and authentic, at gigs she was loud and energetic, as a teacher she helped students believe in themselves. You might have danced with her when she was a ‘two pot screamer’, heard her hoot the theme song of Giggle and Hoot in your lounge room or planted a garden with your family inspired by her heart-song, dirtgirlworld. As the creator of dirtgirlworld and Get Grubby TV, she is a weaver of stories that don’t just inspire dreams of unicorns or hot potatoes. She understands the power of how to tell a story and how that story can influence a generation and shape a better now! About dirtgirl: What happens when you cross David Attenborough with P!nk? You get a person like no one else on this planet, what you get is dirtgirl! She is an unreal pop star with a very real heart and a hyperreal tribe of millions that she reaches everyday. She is also a local and her home, dirtgirlworld, is experiencing the drought and the impact of bush fire too. Seen on TV in 128 countries around the world, she is Australia’s best kept secret and a hero to families across the nation. In the last few months alone, she has broadcast at sunrise from Uluru, tracked waste on the beaches of the Great Barrier Reef, planted fruit trees in the desert and met with the Environment Minister in Canberra to discuss a national approach to recycling. She is walking the walk and talking the talk. For 10 years, dirtgirl has connected with young children and families across her socials and through her shows Get Grubby TV and dirtgirlworld, inspiring and encouraging them to step outside and experience nature and sustainability in everyday life. Not only has she permeated the hearts and backyards of many the country over, this unique, positive-pop eco-warrior has also been widely recognised by the industry, notching up a host of award nominations for Logies, ARIAS and even a BAFTA. dirtgirl has won over audiences and industry abroad too, with the values-filled, nature-connected, family-friendly show airing on televisions across the globe. And tucked up on a shelf in her house is one of the 20 Emmy’s that Australia boasts, after Gene Simmons presented the coveted award to the team Children and Young People category. If you ask her, dirtgirl won’t say she is a hero or a warrior or even a pop star. She identifies as a gardener; an earth dweller who loves singing as much as she loves planting trees, creating compost and going outside and getting grubby, and she lives by the mantra that little things make a big difference, but we happen to think she’s a certified superstar that this planet cannot live without and the newest generation’s true leader of change. dirtgirl will be at Kids Corner at Ewingar Rising on Sunday 24th November from 11am - 1.30pm.',
    "Col Finley is one of Australia's most successful independent recording and touring artists. With over 25 years in the music industry he has recorded and released six very successful commercial albums including his current album The Collective. Col has topped most Australian charts and notably was the first Independent country male artist to top the Australian ARIA Pop Charts. This award-winning singer songwriter and entertainer’s sound has been referred to as “old school, honest Country Rock”. Col's reputation as a brilliant onstage performer is second to none as his ability to entertain his audience is confirmed by the fans, he’s kept over 25 years. He is a real crowd pleaser and will be rocking us on Sunday afternoon 24/11.",
    "Red Belly Black These guys will get you ROCKING!! Hailing from the Northern Rivers, Red Belly Black fuse elements of blues, rock, folk and much more into their own contemporary Australian sound. Can't wait to get these guys on stage!",
  ];

  let imgs = ['great-success.png', 'logo-512.png'];

  let names = ['Tex Perkins', 'Marshall Okell', 'Col Finley'];

  let divs = [
    { name: '.tex', anime: 'tex--animation' },
    { name: '.marsh', anime: 'marsh--animation' },
    { name: '.august', anime: 'august--animation' },
    { name: '.watling', anime: 'watling--animation' },
    { name: '.twotears', anime: 'jimmy--animation' },
    { name: '.jimmy', anime: 'twotears--animation' },
    { name: '.haystack', anime: 'haystack--animation' },
    { name: '.red1', anime: 'red1--animation' },
    { name: '.red2', anime: 'red2--animation' },
    { name: '.red3', anime: 'red3--animation' },
    { name: '.red4', anime: 'red4--animation' },
    { name: '.red5', anime: 'red5--animation' },
  ];

  onMount(() => {
    const options = {
      root: null,
      thresholds: 0.75,
      rootMargin: '0px',
    };

    const lines = document.querySelector('.tex');

    const observer = new IntersectionObserver((entries, observer) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          setTimeout(() => {
            for (let i = 0; i < divs.length; i++) {
              console.log(divs[i].name);
              document.querySelector(divs[i].name).classList.add(divs[i].anime);
            }
          }, 1000);

          setTimeout(() => {
            opac = 1;
          }, 6000);
        }
      });
    }, options);

    observer.observe(lines);
  });
</script>

<div class="content">
  <div class="holder">
    <p class="tex">Ash Grunwald</p>
  </div>
  <div class="holder">
    <p class="marsh">Col Finley &nbsp;&#8226;&nbsp; Matt Scullion</p>
  </div>
  <div class="holder">
    <p class="august">Marshall Okell &nbsp;&#8226;&nbsp; mermaid avenue</p>
  </div>
  <div class="holder">
    <p class="watling">Tullara &nbsp;&#8226;&nbsp;August river band</p>
  </div>
  <div class="holder">
    <p class="jimmy">the band woodshed &nbsp;&#8226;&nbsp; mandy nolan</p>
  </div>
  <div class="holder">
    <p class="twotears">jimmy willing & the real gone hick-ups</p>
  </div>
  <div class="holder">
    <p class="haystack">two tears in a bucket &nbsp;&#8226;&nbsp; nadarra</p>
  </div>

  <div class="holder">
    <p class="red red1">haystack mountain hermits</p>
  </div>
  <div class="holder">
    <p class="red red2">the clarence river mammas</p>
  </div>
  <div class="holder">
    <p class="red red3">aine tyrrell &nbsp;&#8226;&nbsp; red belly black</p>
  </div>
  <div class="holder">
    <p class="red red4">the jacksons &nbsp;&#8226;&nbsp; jonah earley</p>
  </div>
  <div class="holder">
    <p class="red red5">
      highly strung puppets & more ...
      <br /><br />
      <Button href="/artists" square line color="#1ab16a" textColor="white"
        >Details</Button
      >
    </p>
  </div>
  <br />
</div>

<style lang="scss">
  $color-artist: rgb(240, 240, 240);
  .content {
    position: relative;
    top: -20px;
    /* top: 50%;
    left: 50%;
    transform: translate(-50%, -50%); */
  }

  .holder {
    position: relative;
    color: $color-artist;
    margin: 0;
    width: max-content;
    font-family: 'Raleway', serif;
    font-weight: 100;
    padding: 0px;
    left: 50%;
    transform: translateX(-50%);
    text-transform: uppercase;
  }

  .holder p {
    opacity: 0;
    line-height: 1.4rem;
  }

  .holder span {
    cursor: pointer;
  }

  .tex {
    font-size: 4.4rem;
    padding-bottom: 1.4rem;
    position: relative;
    top: 1.3rem;
    border-bottom: 1px solid $color-artist;
  }

  .marsh {
    font-size: 2.2rem;
    // transform: translateY(-14px);
    padding-bottom: 0.9rem;
    border-bottom: 1px solid $color-artist;
  }

  .august {
    font-size: 1.8rem;
    padding-bottom: 0.9rem;
    border-bottom: 1px solid $color-artist;
  }
  .watling {
    font-size: 1.75rem;
    padding-bottom: 0.9rem;
    border-bottom: 1px solid $color-artist;
  }
  .twotears {
    font-size: 1.3rem;
    padding-bottom: 0.9rem;
    border-bottom: 1px solid $color-artist;
  }
  .jimmy {
    font-size: 1.2rem;
    padding-bottom: 0.9rem;
    border-bottom: 1px solid $color-artist;
  }
  .haystack {
    font-size: 1.4rem;
    padding-bottom: 0.9rem;
    border-bottom: 1px solid $color-artist;
  }
  .red {
    font-size: 1.2rem;
    padding-bottom: 0.9rem;
    border-bottom: 1px solid $color-artist;
  }
  .more {
    font-size: 1.2rem;
    padding-top: 0.6rem;
    color: $color-artist;
  }
  .red1,
  .red2,
  .red3,
  .red4 {
    color: $color-artist;
  }
  .red5 {
    border-bottom: 0px solid $color-artist;
  }

  .dialog {
    height: 94vh;
    width: 94vw;
    position: relative;
    background-color: rgba(255, 255, 255, 0.1);
    padding: 1vh 1vw;
    transform: translate(-102%, -102%);
  }

  .dialog-content {
    position: relative;
    background-color: rgba(255, 255, 255, 0.95);
    color: black;
    width: 100%;
    height: 100%;
  }

  .dialog-content h1 {
    font-size: 2.4rem;
  }

  .dialog-content p {
    font-size: 1rem;
  }

  @media only screen and (max-width: 600px) {
    .content {
      padding-top: 28px;
    }
    .holder p {
      margin-top: -0.8rem;
      line-height: 1.1rem;
    }
    .tex {
      font-size: 2.2rem;
      margin-bottom: 2.3rem;
    }
    .marsh {
      font-size: 1.15rem;
      padding-top: 0.4rem;
      // border-top: 1px solid white;
    }
    .august {
      font-size: 0.9rem;
      padding-top: 0.3rem;
      // border-top: 1px solid white;
    }
    .watling {
      font-size: 0.9rem;
      padding-top: 0.5rem;
      // border-top: 1px solid white;
    }
    .twotears {
      font-size: 0.7rem;
      padding-top: 0.7rem;
      // border-top: 1px solid white;
    }
    .jimmy {
      font-size: 0.68rem;
      padding-top: 0.3rem;
      // border-top: 1px solid white;
    }
    .haystack {
      font-size: 0.7rem;
      padding-top: 0.6rem;
      // border-top: 1px solid white;
    }
    .red {
      font-size: 0.7rem;
      padding-top: 0.6rem;
      // border-top: 1px solid white;
    }
  }

  @media only screen and (min-width: 601px) and (max-width: 920px) and (orientation: landscape) {
    .content {
      padding-top: 20px;
    }
    .holder p {
      margin-top: -1rem;
    }
    .tex {
      font-size: 1.4rem;
    }
    .marsh {
      font-size: 1rem;
      padding-top: 0.3rem;
      // border-top: 1px solid white;
    }
    .august {
      font-size: 0.9rem;
      padding-top: 0.3rem;
      // border-top: 1px solid white;
    }
    .watling {
      font-size: 0.75rem;
      padding-top: 0.3rem;
      // border-top: 1px solid white;
    }
    .twotears {
      font-size: 0.7rem;
      padding-top: 0.3rem;
      // border-top: 1px solid white;
    }
    .jimmy {
      font-size: 0.6rem;
      padding-top: 0.3rem;
      // border-top: 1px solid white;
    }
    .haystack {
      font-size: 0.7rem;
      padding-top: 0.3rem;
      // border-top: 1px solid white;
    }
    .red {
      font-size: 0.6rem;
      padding-top: 0.3rem;
      // border-top: 1px solid white;
    }
  }
</style>
