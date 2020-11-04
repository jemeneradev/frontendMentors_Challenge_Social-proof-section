<style>
 /*  .intro,
  .intro__content {
    outline: solid 0.05rem red;
  } */

  .intro {
    position: relative;
    width: 375px;
    height: 316px;

    font-family: "Spartan", sans-serif;
    /* display: flex;
		flex-direction: column;
		justify-content: center; */
    /* background-color: red;
		opacity:.4; */
  }

  .intro__content {
    width: 326px;
    height: 219px;
    margin: 0 auto;
  }

  .intro h1 {
    position: relative;
    margin: 0 auto;
    padding-top: 2.63em;

    /* 10,000+ of our users love our products. */

    font-family: Spartan;
    font-style: normal;
    font-weight: 700;
    font-size: 32px;
    line-height: 101.1%;
    /* or 32px */
    text-align: center;
    letter-spacing: -0.038em;

    color: #511f50;

    /* width: 90%; */
    /* top: 25.5%;
    left: 37px; */

    color: hsl(300, 43%, 22%);

    width: 261px;
    /* color: red;
    opacity: 0.3; */
  }

  .intro p {
    margin: 0 auto;
    /* font-weight: 500;
    font-size: 15px;
    line-height: 167%;
    text-align: center;
    letter-spacing: -0.035em; */

    /* We only provide great products combined with excellent customer service. See what our satisfied customers are saying about our services. */
    width: 326px;
    height: 100px;

    font-family: Spartan;
    font-style: normal;
    font-weight: 500;
    font-size: 15px;
    line-height: 170%;
    /* or 25px */
    margin-top: 23px;
    text-align: center;
    letter-spacing: -0.035em;

    color: hsl(303, 10%, 53%);
  }

    @media screen and (min-width: 1440px) {
    .intro {
      position: relative;
      width:660px;
      height: 396px;
    }

    .intro__content {
      position: relative;
      top: 133px;
      left: 66px;
      width: 462px;
      height: 237px;
      letter-spacing: 0em;
    }
    .intro__content h1 {
      top: 0;
      left: 0;
      margin: 0;
      padding: 0;
      text-align: left;
      font-size: 48px;
      width: 400px;
      height: 150px;
    }
    .intro__content p {
      margin: 0;
      margin-top: 6px;
      padding: 0;
      width: 460px;
      height: 80px;
      text-align: left;
    }
  }
</style>

<div class="intro">
  <div class="intro intro__content">
    <h1>10,000+ of our users love our products.</h1>
    <p>
      We only provide great products combined with excellent customer service.
      See what our satisfied customers are saying about our services.
    </p>
  </div>
</div>
