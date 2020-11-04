<script>
  export let stars = 5;
  export let loc = 0;
  export let desc = "";
</script>

<style>
  /* .reviews,
  .review,
  .review p,
  .review .review__stars {
    outline: solid 0.5px black;
  } */

  .review {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;

    margin-bottom: 16px;
    width: 326px;
    height: 78px;

    background-color: hsl(300, 24%, 96%);

    /* background-color: red;
    opacity: 0.4; */
    border-radius: 8px;
  }

  .review p {
    font-family: "Spartan", sans-serif;
    font-weight: 700;
    color: hsl(300, 43%, 22%);
   /*  color: red; */
    font-size: 13px;
    margin-top: 16px;
    margin-left: 0px;
    width: 274px;
    height: 13px;
    text-align: center;
  }

  .review .review__stars {
    color: #EF9546;
    background-image: url(images/icon-star.svg);
    /* background-repeat: no-repeat; */
    background-position: -1px 0px;
    background-size: 25px 17px;
    background-clip: content-box;
    margin: 0;
    margin-top: 16px; /* 
    margin-bottom: 6px; */

    width: calc(25px * var(--data-stars));
    /**/
    height: 50px;
    border-radius: 0;
  }

  /* .review .review__stars img {
      margin-left: 0px;
      margin-right: 4px;
    } */

  .review .review__stars img:last-child {
    margin-right: 0px;
  }

  @media screen and (min-width: 1440px) {
    .review {
      flex-direction: row;
      height: 56px;
      width: 445px;
      margin-left: calc(48px * var(--data-indent));
      margin-bottom: 16px; /* 
        opacity: .5;
        background-color: red; */
    }

    .review .review__stars {
      margin-top: -2px;
      margin-left: 28px;
      margin-right: 30px;
      height: 16px;
    }

    .review p {
      margin-top: 14px;
      margin-left: 2px;
    }

    .review .review__stars{
     /*  opacity: .3;
      color: red; */
      background-size: 25px 16px;
    }
  }
</style>

<div class="review" style={`--data-stars:${stars};--data-indent:${loc};`}>
  <div class="review review__stars" />
  <p class="review">{`${desc}`}</p>
</div>
