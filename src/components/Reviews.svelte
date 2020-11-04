<script>
  import Review from "./Review.svelte";

  let reviews = [
    {
      stars: 5,
      desc: "Rated 5 Stars in Reviews",
    },
    {
      stars: 5,
      desc: "Rated 5 Stars in Report Guru",
    },
    {
      stars: 5,
      desc: "Rated 5 Stars in BestTech",
    },
  ];
</script>

<style>
 /*    .reviews,
    .reviews ul,
    .reviews ul li {
    outline: solid .5px black;
  } */
  .reviews {
    width: 375px;
    height: 316px;
  }
  .reviews ul {
    width: 327px;
    height: 266px;
    margin: 0 auto;
    margin-top: 25px;
    margin-bottom: 25px;
    padding: 0;
  }

  .reviews ul li {
    list-style: none;
  }

  @media screen and (min-width: 1440px) {
    .reviews {
    width: 780px;
    height: 396px;
    position: relative;
  }

  .reviews ul {
      position: relative;
      width: 540px;
      height: 200px;
      left: 75px;
      top: 148px;
      margin: 0;
  }
  }
</style>

<div class="reviews">
  <ul>
    {#each reviews as r, index}
      <li>
        <Review stars={r.stars} loc={index} desc={r.desc} />
      </li>
    {/each}
  </ul>
</div>
