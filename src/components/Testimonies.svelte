<script>
  import Testimony from "./Testimony.svelte";

  let testimonies = [
    {
      client: "Colton Smith",
      pic: "./images/image-colton.jpg",
      opinion:
        "We needed the same printed design as the one we had ordered a week prior. Not only did they find the original order, but we also received it in time. Excellent!",
    },
    {
      client: "Irene Roberts",
      pic: "./images/image-irene.jpg",
      opinion:
        "Customer service is always excellent and very quick turn around. Completely delighted with the simplicity of the purchase and the speed of delivery.",
    },
    {
      client: "Anne Wallace",
      pic: "./images/image-anne.jpg",
      opinion:
        "Put an order with this company and can only praise them for the very high standard. Will definitely use them again and recommend them to everyone! ",
    },
  ];
</script>

<style>
  /*     .reviews,
      .reviews ul,
      .reviews ul li {
      outline: solid .5px black;
    } */
  .testimonies {
    width: 375px;
    height: 316px;
  }
  .testimonies ul {
    width: 327px;
    height: 266px;
    margin: 0 auto;/* 
    margin-top: 50px; */
    padding: 0;
  }

  .testimonies ul li {
    list-style: none;
    margin-bottom: 16px;
  }

  @media screen and (min-width: 1440px) {
    /* .testimonies {
      width: 1440px;
      height: 404px;
    } */

    .testimonies ul {
      display: flex;
      flex-direction: row;
      margin: 0;
      margin-left: 165px;
      margin-top: 34px;
    }

    .testimonies ul li {
        margin-right: 30px;
    }
  }
</style>

<div class="testimonies">
  <ul>
    {#each testimonies as t, index}
      <li>
        <Testimony client={t.client} pic={t.pic} opinion={t.opinion} loc={index}/>
      </li>
    {/each}
  </ul>
</div>
