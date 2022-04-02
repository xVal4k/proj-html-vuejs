<template>
  <section id="sec_1">
    <img v-for="photo in photos" :key="photo.alt" :src="photo.src" :alt="photo.alt">
  </section>
</template>

<script>
/* eslint-disable */

import newPlace from "../../assets/images/img/h3-img-1.jpg";
import eatGoodPizza from "../../assets/images/img/h3-img-2.jpg";
import yumYumYum from "../../assets/images/img/h3-img-3.jpg";
import biggestPizza from "../../assets/images/img/h3-img-4.jpg";

export default {
  name: 'Section1',
  data () {
    return {
      photos: [
        {
          src: newPlace,
          alt: 'new place photo'
        },
        {
          src: eatGoodPizza,
          alt: 'eat good pizza photo'
        },
        {
          src: yumYumYum,
          alt: 'yum yum photo'
        },
        {
          src: biggestPizza,
          alt: 'biggest pizza photo'
        },
      ]
    }
  }
}
</script>

<style scoped lang="scss">
#sec_1 {
  display: flex;
  flex-wrap: wrap;
  gap: .5rem;
  padding: .5rem 0;
  img {
    width: calc((100% - 1.5rem) / 4);
  }
}
</style>
