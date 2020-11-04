<script>
  export let client = "Past Customer";
  export let opinion = "";
  export let pic = "";
  export let loc = 0;
</script>

<style>
/*   .testimony,
  .testimony__contact,
  .testimony__contact__pic
  .testimony__quotebody {
    outline: solid .5px white;
  } */
  .testimony {
    position: relative;
    width: fit-content;
    height: 248px;
    width: 327px;

    background: hsl(300, 43%, 22%);
    /* background-color: red; */
    /* opacity: .3; */

    border-radius: 8px;

    margin: 0;
    padding: 0;

    /* top: 657px;
    left:24px */
  }

  .testimony .testimony__contact {
    position: relative;
    width: 100%;
    height: 5.9375em; /*95px*/
    display: flex;
    font-family: "Spartan", sans-serif;

    /* 95px */
    /* position: relative;
      display: flex;
      font-family: 'Spartan', sans-serif;

      margin: 0;
      width: 90%; */
    /* opacity: .5; */
  }

  .testimony .testimony__contact .testimony__contact__pic {
    position: relative;
    width: 85px;
    height: 95px;
    margin: 0;
    top: 0;
    left: 0;
  }
  .testimony .testimony__contact .testimony__contact__pic img {
    width: 40px;
    height: 40px;
    border-radius: 50%;
    position: relative;
    top: 40px;
    left: 32px;
  }

  .testimony .testimony__contact .testimony__contact__info {
    width: 242px;
    height: 95px;
    position: relative;
    display: flex;
    flex-direction: column;
    padding-left: 13px;
  }

  .testimony .testimony__contact .testimony__contact__info h1 {
    width: 216px;
    height: 19px;
    color: hsl(300, 24%, 96%);
    margin: 0;
    padding-top: 41px;
    font-family: Spartan;
    font-style: normal;
    font-weight: 700;
    font-size: 13px;
    line-height: 166%;
    /* or 22px */
    /* letter-spacing: -0.005em; */
    letter-spacing: 0em;
  }

  .testimony .testimony__contact .testimony__contact__info h2 {
    width: 216px;
    height: 19px;
    margin: 0;
    margin-top: 1px;

    font-family: Spartan;
    font-style: normal;
    font-weight: 500;
    font-size: 13px;
    line-height: 166%;
    /* or 22px */
    /* letter-spacing: -0.012em; */
    letter-spacing: 0em;
    color: hsl(333, 80%, 67%);
  }

  .testimony .testimony__quote {
    margin: 0;
    position: relative;
    width: 327px;
    height: 130px;
    top: 0;

    /* padding-top: 12px;
    padding-left: 8px */;
  }

  .testimony .testimony__quote blockquote {
    margin: 0;
    padding: 0;
    margin-top: 12px;
    margin-left: 32px;
    /* top: 12px;
    left: 16px; */
    width: 263px;
    height: 135px;
    word-spacing: 0.011em;
    color: hsl(300, 24%, 96%);
    /* color: black; */


/*     width: 265px;
    height: 110px; */

    font-family: Spartan;
    font-style: normal;
    font-weight: 500;
    font-size: 13px;
    line-height: 22px;
    letter-spacing: -0.022em;
  } 
/*   .testimony .testimony__quote {
    font-family: "Spartan", sans-serif;
    font-weight: 500;
    font-size: 13px;



    color: hsl(300, 24%, 96%);
  } */

  .testimony .testimony__quote blockquote::before {
    content: "“";
    position: relative;
    left: 0px;
  }

  .testimony .testimony__quote blockquote::after {
    content: "”";
  }

  /* @media screen and (min-width: 1440px) {
    .testimony {
      width: 351px;
      height: 235px;
      margin-left: 28px;
      margin-top: calc(16px * var(--data-testimony-index));
    }

    .testimony .testimony__quote {
      width: 285px;
    }
  } */

  @media screen and (min-width: 1440px) {
    .testimony {
      /* background-color: red; */
      /* opacity: .3; */
      width: 350px;
      height: 234px;
      margin-top: calc(16px * var(--data-indent));
    }
    .testimony .testimony__quote{
      height: 115px;
    }
    
    .testimony .testimony__quote blockquote {
      /* margin: 0; */
      width: 88%;
    }
  }

</style>

<div class="testimony" style={`--data-indent:${loc};`}>
  <div class="testimony__contact">
    <div class="testimony testimony__contact testimony__contact__pic">
      <img src={pic} />
    </div>
    <div class="testimony__contact testimony__contact__info">
      <h1>{client}</h1>
      <h2>Verified Buyer</h2>
    </div>
  </div>
  <div class="testimony testimony__quote">
    <blockquote>{' ' + opinion + ' '}</blockquote>
  </div>
</div>
