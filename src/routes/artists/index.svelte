<script lang="ts">
  import Nav from '$lib/components/Nav.svelte';

  let array = [
    {
      id: 0.3,
      name: 'Ash Grunwald',
      image: '/ashGrunwald.png',
      some: `<p>With the liberation that comes from many lineages pouring into one; not confined by the borders of race nor the parameters of culture, Ash Grunwald is an advocate purely and simply of the Earth. His music, whilst calling from the Delta Swamp, is an eddy of influences, collaborations and mediums. His voice through his lyrics, podcast and broadcasting ask for the protection of land, sea, river, self and resources, and his new role as an author signifies the sudden abundance of purpose that comes with sobriety and of a man carrying a message of change.</p>
<p>Under the guidance of his grandfather, Ash learned to play guitar and bass as a young child, together recording his first ever song - a cover of Howlin’ Wolf’s ‘Going Down Slow’.</p> <p>At age 26, after his brief but enriching start to adulthood as a secondary school teacher (which confirmed his aversion to having a day job), Ash Grunwald cemented his change in career with the release of his first album, Introducing, a solo affair consisting of one guitar, one man and a stomp box. Introducing was followed not long after by his second album I Don’t Believe, defining Ash as a soulful bluesman far beyond his years who possessed the enthusiastic fervour of a young modern technologist.</p>
<p>Throughout his career, Ash has received five ARIA Award nominations and a swag of other award wins including MBAS Blues Performer Of The Year (2003), and the AIR Best Independent Blues And Roots Album for 2010’s, Hot Mama Vibes. The first single ‘Walking’ from the latter album, featured prominently in the Hollywood blockbuster ‘Limitless’, which starred Robert De Niro and Bradley Cooper.</p>
<p>Ash Grunwald has carved out a unique path that inspires others to do the same - to follow passions from one project to the next, expanding skills and themselves as an individual, whilst also serving the greater good. With this mindset, Ash Grunwald released his first ever book - Surf By Day, Jam By Night – published by Pantera Press in August 2019. </p>`,
    },
    {
      id: 1,
      name: 'Col Finley',
      image: '/colFinley.jpg',
      some: `<p>Col Finley is one of Australia's most successful independent recording and touring artists.</p>
<p>With over 25 years in the music industry he has recorded and released six very successful commercial albums including his current album The Collective.</p>
<p>Col has topped most Australian charts and notably was the first Independent country male artist to top the Australian ARIA Pop Charts. This award-winning singer songwriter and entertainer’s sound has been referred to as “old school, honest Country Rock”.</p>
<p>Col's reputation as a brilliant onstage performer is second to none as his ability to entertain his audience is confirmed by the fans, he’s kept over 25 years.</p>`,
    },
    {
      id: 2,
      name: 'Matt Scullion',
      image: '/mattScullion.jpg',
      some: `<p>Matt Scullion is a Golden Guitar winning Australiana singer/songwriter with 21 number one songs to his credit. </p>
<p>Originally hailing from Ulladulla on the South Coast of NSW. Matt has had his songs recorded by the cream of Australian Country including- Lee and Tania Kernaghan, Sara Storer, Adam Harvey, Travis Collins and Amber Lawrence to name but a few. Cold Chisel even recorded one of Matt”s songs on their 2015 album “The Perfect Crime”. His 2019 ten-track album AUSSIE AS, produced by 
award-winning producer Shane Nicholson has been received with open arms by critics and fans alike. It spawned 4 chart-topping singles, with the title track “Aussie As” and the infectious tongue-in-cheek singalong “Slanguage” both shooting to NO 1 while being aired heavily on The Ray Hadley Show.</p>`,
    },
    {
      id: 3,
      name: 'Tullara',
      image: '/tullara.jpg',
      some: `<p>Home grown in Northern NSW and now based out of Cairns QLD, Tullara has been making her mark across the Australian music industry since her debut release 'Better Hold On' in 2016.  Winning "BEST EP" at the 2017 'Australian Roots Music Awards', and independently reaching over 1,000,000 streams on Spotify in 2018, Tullara has since racked up performances at some of Australia’s largest and most respected music festivals including: Woodford Folk Festival, Queenscliff Music Festival, Mullum Music Festival, and Bendigo Blues & Roots Festival, just to name a few. </p>
<p>In 2018/19, Tullara played 310 shows across the country including support slots for International Artists Donavon Frankenreiter (USA), Wallis Bird (IRE) and The East Pointers (CAN), as well as Aussie Folk legends The Waifs, Jeff Lang, Troy Cassar-Daley, & Mia Dyson.</p>
<p>With her percussive finger tapping, guitar playing wizardry, not to mention the alluring power of her voice, Tullara has an undeniable, uniquely endearing stage presence of full raw, powerful honesty, and swagger. Along with her all female, dynamic trio, Tullara takes the genre of Folk/Roots to a whole new level.</p>`,
    },
    {
      id: 4,
      name: 'Marshall Okell',
      image: '/marshallOkell.jpg',
      some: `<p>With up to 200 live gigs a year as part of his repertoire, Marshall has developed into an Aussie rocking bluesman like no other. His ever expanding list of musical accolades includes awards for the 2012 ‘Best Blues & Roots Artist’ at the Oz Music Awards. He has also been a winner of the of ‘Album of the Year’, ‘Song of the Year’, ‘Best Male Vocal’, ‘Best Protest’ and ‘Best Blues & Roots Artist’ at the NCEIA Dolphin Awards.
Based out of Byron Bay, Marshall combines his love for legendary Soul and Blues singers like Little Feat, The Allman Brothers, Hat Fitz, Mavis Staples and Muddy Waters, with his undisguisable Hendrix, 70’s Woodstock sound.</p>
<p>“The result is a deep, raw, honest, dirty blues sound that grabs you by the throat and then sooths you with a sweet honey tasting musical medicine. There are pure guts, sweat and emotion in his latest material that leave you exhausted and elated in their wake.”</p>`,
    },
    {
      id: 5,
      name: 'August River Band',
      image: '/augustRiverBand.jpg',
      some: `<p>August River Band hail from QLD and are a three-piece outfit, with tightly arranged odd time signatures dissolving into soaring choruses which unapologetically push the boundaries of the alternative folk genre, whilst maintaining a soulful beckoning of the dark and the beautiful. Described as “Like crying whilst dancing”…</p>
<p>August River Band offers a wild and beautifully juxtaposed chemistry between the tortured singer-songwriter, the classically trained violinist and the hard-hitting rock and roll drummer. Major influences range from The Police, Dave Matthews, Midnight Oil, Edward Elgar, Foo Fighters and Radiohead.</p>`,
    },
    {
      id: 6,
      name: 'The Band Woodshed',
      image: '/artistsBG.png',
      some: `<p>"Woodshed (verb) to practise on a musical instrument.”</p>
<p>The Band Woodshed are an off the cuff drunken jam sparked the inception of Woodshed.</p>
<p>With a love for blues, country and classic rock’n’roll, the Brisbane trio have their own unique sound infused with raucous, upbeat, cowpunk rhythms and blues rock.</p>
<p>Woodshed has two EP releases, and have performed at various big festivals including Byron Bay Bluesfest.</p>`,
    },
    {
      id: 7,
      name: 'Two Tears in a Bucket',
      image: '/twoTears.jpg',
      some: `<p>Two Tears in a Bucket are Northern Rivers locals, with Michelle Fitness and Nathan Peterson at their core, often accompanied by Matt Elliot and Miss Jodie. This has been a popular band over the years, playing in venues across the region. Two Tears in a Bucket explore blues and roots and sing and play from the depths of their souls.</p>`,
    },

    {
      id: 8,
      name: 'Mandy Nolan',
      image: '/mandyNolan.jpg',
      some: `<p>Mandy Nolan is a true renaissance woman. Comedian, Author, Journalist, MC, KeyNote Speaker, Humour Therapist & Comedy Instructor.</p>

<p>A stand-up comedian for well over 28 years, audiences adore Mandy on stage…her humour is sharp, honest, sometimes self-depreciating, somewhat outrageous, but never cruel or pretentious. Frequently irreverent, it speaks to a diverse audience with no set demographic, no gender, race or religion, occupation or tribe.
One of Australia’s strongest female comedic talents, Mandy Nolan has honed the ability to bring a room to its knees, whether that be Melbourne’s Last Laugh, Gold Coast’s Comedy in the Basement, Brisbane’s Sit Down Comedy Club, the 2000 plus crowds she’s wowed at Jupiter Casino’s Laugh Your Pants Off Gala’s or the 800 strong function of women from VIEW club who all declared Nolan hands down the funniest guest speaker they’d ever had.</p>

<p>A self-proclaimed expert on all matters feminine, Mandy writes for the Byron Echo where her weekly Soapbox has attracted the admiration and loyalty of readers for almost two decades. Nolan also writes for Mamamia, was a contributor for Wendy Harmer’s Online magazine The Hoopla and has been a featured guest on ABC’s Q&A and SBS’s Mums The Word.</p>

<p>Nolan’s most important work however is the unique Stand Up for Dementia, the Humour Therapy she created for people with dementia that was developed with the assistance of Commonwealth funding with research making its way International peer reviewed medical journals. Most recently Nolan was featured on SBS’s Insight for her innovative approach to working with people with high levels of dementia.</p>

<p>With her keen eye for detail and dark wit, Mandy excels in what she calls ‘a dangerous social autopsy!’ If you like David Sedaris and Jennifer Lawson, if you like outrageous observations peppered with intelligent insightful quips, then you’ll love Mandy Nolan.`,
    },
    {
      id: 9,
      name: 'Jimmy Willing and the Real Gone Hick-Ups',
      image: '/jimmyWilling.jpg',
      some: `<p>Jimmy Willing & the Real Gone Hick-Ups are a local Northern Rivers band who tend to throw the crowd sideways and get everyone jumping!!</p>
<p>They are as unique as they come, with their Rockabilly/Ska/Country style music that will not allow any toe to sit idle. This band is very popular in the Northern Rivers as they entertain like no other.</p>`,
    },
    {
      id: 10,
      name: 'Haystack Mountain Hermits',
      image: '/haystackMountainHermits.jpg',
      some: `<p>Haystack Mountain Hermits are a local full family band made up of mum, dad and four kids, playing an eclectic mix of instruments, voices and repertoire producing a unique sound which has been described as Hermit Happiness.</p>
<p>They have won numerous busking championships over the past couple of years, including the Australian National Busking Championships, and are the first ever act to win Tamworth and ANBC in the same year.</p>`,
    },
    {
      id: 11,
      name: 'Aine Tyrrell',
      image: '/aineTyrrell.jpg',
      some: `<p>Australia’s favourite adopted Irish sister, Áine Tyrrell is a modern day Pirate Queen, except instead of ships, she captures audiences, one heart at a time. Her latest offering Return to the Sea was written and recorded in her homeland but mastered and crowdfunded with one boot in the red dirt of Australia. The album is alive with contemporary narratives rising from a solid respect for tradition. Critics worldwide lauding Tyrrell as a force of nature and this album full of anthems for humanity. Return To The Sea is a call to arms, a sirens wisdoms and warnings, and most importantly the soundtrack of a woman who walks her own beat. 
Following the release of the single "In This House" in 2019 with over 18,000 entries Tom Waits voted her not only as a finalist in the International Songwriting Competition, but she received the much-coveted honourable mention in the Singer-Songwriter Category. Her exceptional musicianship and an equally deft touch with a killer hook or a heartrending lament has also garnered critical acclaim from national radio outlets in both Ireland and Australia with multiple radio appearances on ABC Radio, RTE Radio, Double J Radio, and BBC NI Music.  ‘Don’t Be Left Crying’ the single from Fledgling Fall in 2017 climbed to Number One on Ireland’s national broadcaster RTE’s Independent Music Charts. </p>
<p>Aine is also known for the constantly sold out feminist re-imagining of a women’s association meeting aptly named the Country Witches Association, in partnership with co-founding witch and comedian Mandy Nolan.</p>`,
    },
  ];

  function handleClick(params) {
    let elem = document.getElementById('dialog');
    elem.style.height = '90vh';
    elem.style.overflow = 'scroll';
    let pic = document.getElementById('artistPic');
    pic.style.background = `url(${params.image})`;
    pic.style.backgroundSize = 'cover';
    pic.style.backgroundPosition = '50% 25%';
    let name = document.getElementById('name');
    name.innerHTML = params.name;
    let some = document.getElementById('some');
    some.innerHTML = params.some;
    let close = document.getElementById('close');
    close.style.display = 'block';
    let bg = document.getElementById('dialog--bg');
    bg.style.height = '100vh';
    bg.style.width = '100vw';
    bg.style.top = '0';
    bg.style.left = '0';
  }

  function handleClose() {
    let elem = document.getElementById('dialog');
    elem.style.height = '0px';
    elem.style.overflow = 'hidden';
    let close = document.getElementById('close');
    close.style.display = 'none';
    let bg = document.getElementById('dialog--bg');
    bg.style.height = '0px';
    bg.style.width = '0px';
    bg.style.top = '50%';
    bg.style.left = '50%';
  }
</script>

<Nav />
<div class="content">
  <div class="content--bg" />
  <div class="content--holder">
    <div class="content--intro">
      <h1>Ewingar Rising Artist Lineup</h1>

      <p class="content--intro__para">
        Below are all the artists currently confirmed to be playing at Ewingar
        Rising <br />Click on an artist to see a bio and when they are playing.
        <br />This list is subject to change and please check back here as we
        continue to add new artists to this list.<br />
      </p>
      <br />
      <!-- <br />
      <div class="content--line" />
      <br /><br /> -->
    </div>
    <ul class="hex-grid__list">
      {#each array as item}
        <li class="hex-grid__item">
          <div
            class="hex-grid__content"
            style={`background: url('${item.image}'); background-size: cover;`}
            on:click={() => {
              handleClick(item);
            }}
          >
            <p>{item.name}</p>
          </div>
        </li>
      {/each}
    </ul>
    <!-- {#each array as item}
      <div class="artist--bio" id={JSON.stringify(item.id)}>
        <div class="close" on:click={() => handleClose(item)}><h3>X</h3></div>
        <div
          class="artist--pic"
          style={`background: url('${item.image}'); background-size: cover; background-position: 50% 25%;`}
        />
        <div class="artist--bio__details">
          <h1>{item.name}</h1>
          {@html item.some}
        </div>
      </div> -->
    <!-- <div class="hex-grid__content--dialog" id={JSON.stringify(item.id)}>
        <div class="close" on:click={() => handleClose(item)}><h3>X</h3></div>
        <div
          class="artist--pic"
          style={`background: url('${item.image}'); background-size: cover;`}
        />
        <div class="hex-grid__content--dialog__content">
          <h1>{item.name}</h1>
          <p>{item.some}</p>
        </div>
      </div> -->
    <!-- {/each} -->
    <br /><br />
  </div>
</div>

<div class="artist--bio" id="dialog">
  <div class="close" id="close" on:click={handleClose}><h3>X</h3></div>
  <div class="artist--pic" id="artistPic" />
  <div class="artist--bio__details">
    <!-- <h1>{item.name}</h1> -->
    <!-- {@html item.some} -->
    <h1 id="name" />
    <p id="some" />
  </div>
</div>
<div class="dialog--bg" id="dialog--bg" />
<!-- <div class="hex-grid__content--dialog" id={JSON.stringify(item.id)}>
  <div class="close" on:click={() => handleClose(item)}><h3>X</h3></div>
  <div
    class="artist--pic"
    style={`background: url('${item.image}'); background-size: cover;`}
  />
  <div class="hex-grid__content--dialog__content">
    <h1>{item.name}</h1>
    <p>{item.some}</p>
  </div>
</div> -->

<!-- style={`background: url('${item.image}'); background-size: cover; background-position: 50% 25%;`} -->
<style lang="scss" src="../../lib/scss/pages/_artists.scss"></style>
