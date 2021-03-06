<script>
  import TextBlock from "../components/TextBlock.svelte";

  function years(from) {
    return new Date().getFullYear() - new Date(from).getFullYear();
  }
</script>

<style>
  figure {
    text-align: center;
    margin: 0 auto 8.5em auto;
    max-width: 90vw;
  }
  h1,
  figcaption {
    text-transform: uppercase;
    font-weight: 700;
    font-size: 1.2em;
  }
  h1 {
    font-size: 4em;
    margin: 1em 0 0.2em 0;
  }
  figcaption {
    display: inline-block;
    border-top: 2px solid black;
    padding-top: 0.5em;
  }
  img,
  .img-border {
    border-radius: 50%;
    max-width: 100%;
  }
  img {
    position: absolute;
    top: 3px;
    left: 3px;
    width: 20em;
    max-width: calc(100% - 6px);
    margin: 0;
    border: none;
    box-shadow: none;
  }
  .img-wrap {
    display: inline-block;
    position: relative;
    width: calc(6px + 20em);
    max-width: 100%;
  }
  .img-border {
    position: relative;
    width: 100%;
    padding-bottom: 100%;
    background: linear-gradient(
      to bottom right,
      #ffffff,
      #ff614d,
      #ff2a0e,
      #ff0000
    );
    box-shadow: 12px 12px 12px 0px rgba(0, 0, 0, 0.3),
      -12px -12px 12px 0px rgba(255, 255, 255, 0.7);
  }
  i {
    font-style: normal;
  }
  @media (max-width: 480px) {
    h1 {
      font-size: 2em;
    }
    figcaption {
      font-size: 1em;
    }
  }
</style>

<svelte:head>
  <title>Teemu Karppinen</title>
</svelte:head>

<figure>
  <div class="img-wrap">
    <div class="img-border">
      <img alt="My face" src="me2.jpg" />
    </div>
  </div>
  <h1>Teemu Karppinen</h1>
  <figcaption>Fullstack developer, boulderer, sushi fanatic</figcaption>
</figure>

<article>
  <TextBlock>
    <h2 id="i-am" slot="title">
      <i aria-hidden="true">👦</i>
      I am
    </h2>
    <p>
      a web developer from Joensuu, Finland. I am {years('April 5, 1994 00:00:00')}
      years old and I have been doing different kinds of development for {years('August 1, 2015 00:00:00')}
      years. During those {years('August 1, 2015 00:00:00')} years I have
      studied in the university, worked professionally for {years('November 1, 2017 00:00:00')}
      years and spent countless hours continuosly learning and expanding my
      skillset. I am currently working as a lead developer at
      <a href="https://www.processgenius.fi/en/">Process Genius</a>
      - a company developing various industrial IOT web platforms.
    </p>
  </TextBlock>
  <TextBlock>
    <h2 id="my-skillset" slot="title">
      <i aria-hidden="true">💻</i>
      My skillset
    </h2>
    <p>
      is mainly focused on web development, so basically the web trio
      (JS/HTML/CSS), TypeScript and the related tools and frameworks. I do not
      want to define myself as a single framework developer and instead have
      heavily invested into the fundamentals of the web platform. I do, however,
      have most professional frontend experience in the Vue.js ecosystem. On the
      backend I have mostly worked with Drupal, Node.js, Linux servers and some
      Azure. I am currently also dabbling into Serverless and the AWS ecosystem
      on my spare time.
    </p>
  </TextBlock>
  <TextBlock>
    <h2 id="i-enjoy" slot="title">
      <i aria-hidden="true">😍</i>
      I enjoy
    </h2>
    <p>
      experimenting with functional languages like Haskell and trying to bend
      the limits of JavaScript's and TypeScript's FP cabapilities. I also like
      replicating "poor man's versions" of common frameworks and libraries in
      hopes of gaining a deeper understanding of the tools we use to build
      stuff.
    </p>
  </TextBlock>
  <TextBlock>
    <h2 id="to-stay-in-shape" slot="title">
      <i aria-hidden="true">🧗‍♂️</i>
      To stay in shape
    </h2>
    <p>
      I go bouldering, snowboarding and ride my MTB. I am not particularily good
      at any of those but I am having a good time nonetheless!
    </p>
  </TextBlock>
</article>
