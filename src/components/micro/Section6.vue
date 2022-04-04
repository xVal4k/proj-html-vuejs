<template>
  <section id="sec_6">
    <div class="cont">
      <a href="#!">
      <img v-for="logo in logos" :key="logo" :src="logo.src" :alt="logo.alt">

      </a>
    </div>
  </section>
</template>

<script>
/* eslint-disable */
import Cowboy from "../../assets/images/img/h1-clients-img-4.png";
import Gordon from "../../assets/images/img/h1-clients-img-3.png";
import BCheese from "../../assets/images/img/h1-clients-img-1.png";
import Bludoos from "../../assets/images/img/h1-clients-img-2.png";
import Vegan from "../../assets/images/img/h1-clients-img-5.png";

export default {
  name: "Section6",
  data () {
    return {
      logos: [
        {
          src: Cowboy,
          alt: 'Cowboy logo'
        },
        {
          src: Gordon,
          alt: 'Gordon logo'
        },
        {
          src: BCheese,
          alt: 'Big Chese logo'
        },
        {
          src: Bludoos,
          alt: 'Bludoos Bar logo'
        },
        {
          src: Vegan,
          alt: 'Vegan logo'
        },
      ]
    }
  }
};
</script>

<style scoped lang="scss">
#sec_6 {
  background: grey;
  padding: 4rem;
  margin: .5rem 0;
  .cont {
    width: 60%;
    max-width: 1400px;
    margin: 0 auto;
    img {
      width: calc(100% / 5);
    }
  }
}
</style>
