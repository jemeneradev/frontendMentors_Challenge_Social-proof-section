<script>
  import Intro from "./components/Intro.svelte";
  import Reviews from "./components/Reviews.svelte";
  import Testimonies from "./components/Testimonies.svelte";
</script>

<style>
  /*Section Layout Debud*/
  /* .intro {
		background-color: green;
		opacity: .4;
	}
	.reviews {
		background-color: aqua;
		opacity: .4;
	}
	.testimonies {
		background-color: blueviolet;
		opacity: .4;
	} */

  .reviews {
    height: 298px;
  }
  .testimonies {
    height: 830px;
  }

  .solution {
    /* background-color: grey;
		opacity: .4; */
    height: 618px;
    max-width: 375px;
    margin: 0;
    padding: 0;
  }

  @media screen and (min-width: 1440px) {
    .solution {
      position: relative;
      top: -16px;
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-template-rows: 65% 30%;
      gap: 0px 0px;
      grid-template-areas:
        ". ."
        ". .";
    }

    .reviews {
      grid-column: 2/3;
      height: 400px;
    }
    .testimonies {
      grid-column: 1/3;
      height: 400px;
    }
  }

  .top-pattern {
    position: absolute;
    top: 0px;
    z-index: -10;
    fill: blqck;
  }
  .bottom-pattern {
    position: absolute;
    top: 796px;
    z-index: -10;
  }
  @media screen and (min-width: 1440px) {
    .top-pattern {
      top: 9px;
      left: 8px;
    }
    .bottom-pattern {
      top: 138px;
      left: 364px;
    }
  }

  .design {
    position: absolute;
    margin: 0 auto;
    margin-top: -616px; /*Solution Height + 8*/
    z-index: -10;
    /*  background-color: red; */
  }
  .design img {
    margin: 0 auto;
  }
</style>

<main>
  <div class="solution">
    <Intro />
    <Reviews />
    <Testimonies />
    <div class="top-pattern">
      <picture>
        <source
          media="(min-width:1440px)"
          srcset="./images/bg-pattern-top-desktop.svg" />
        <source
          media="(max-width:1439px)"
          srcset="./images/bg-pattern-top-mobile.svg" />
        <img src="./images/bg-pattern-top-mobile.svg" alt="Mobile Design" />
      </picture>
    </div>
    <div class="bottom-pattern">
      <picture>
        <source
          media="(min-width:1440px)"
          srcset="./images/bg-pattern-bottom-desktop.svg" />
        <source
          media="(max-width:1439px)"
          srcset="./images/bg-pattern-bottom-mobile.svg" />
        <img src="./images/bg-pattern-bottom-mobile.svg" alt="Mobile Design" />
      </picture>
    </div>
  </div>
<!--   <div class="design">
    <picture>
      <source media="(min-width:1440px)" srcset="./design/desktop-design.jpg" />
      <source media="(max-width:1439px)" srcset="./design/mobile-design.jpg" />
      <img src="./design/mobile-design.jpg" alt="Mobile Design" />
    </picture>
  </div> -->
</main>
