<template>
  <section id="sec_1">
    <div
      v-for="(photo, index) in photos"
      :key="index"
      class="img_cont"
      @mouseover="setHover(index)"
      @mouseout="imgHover = null"
      @focus="setHover(index)"
      @focusout="imgHover = null"
    >
      <img :src="photo.src" :alt="photo.alt" :class="imgHover == index ? 'display_none' : ''" />
      <div class="hover_eye"><i class="far fa-eye"></i></div>
    </div>
  </section>
</template>

<script>
/* eslint-disable */

import newPlace from "../../assets/images/img/h3-img-1.jpg";
import eatGoodPizza from "../../assets/images/img/h3-img-2.jpg";
import yumYumYum from "../../assets/images/img/h3-img-3.jpg";
import biggestPizza from "../../assets/images/img/h3-img-4.jpg";

export default {
  name: "Section1",
  data() {
    return {
      photos: [
        {
          src: newPlace,
          alt: "new place photo",
        },
        {
          src: eatGoodPizza,
          alt: "eat good pizza photo",
        },
        {
          src: yumYumYum,
          alt: "yum yum photo",
        },
        {
          src: biggestPizza,
          alt: "biggest pizza photo",
        },
      ],
      imgHover: null,
    };
  },
  methods: {
    setHover(index) {
      this.imgHover = index;
    },
  },
};
</script>

<style scoped lang="scss">
#sec_1 {
  padding: 0.5rem 0;
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  .img_cont {
    position: relative;
    width: calc((100% - 1.5rem) / 4);
    background-image: radial-gradient(lightgrey 10%, transparent 11%),
    radial-gradient(#fff 10%, transparent 11%);
    background-size: 10px 10px;
    background-position: 0 0, 30px 30px;
    background-repeat: repeat;
  }
  img {
    width: 100%;
    height: 100%;
    z-index: 9;
    position: relative;
  }
  .hover_eye {
    height: 80px;
    width: 80px;
    font-size: 30px;
    color: white;
    background: red;
    border-radius: 50%;
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    z-index: 0;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
  }
}
.display_none {
  display: none;
}
</style>
