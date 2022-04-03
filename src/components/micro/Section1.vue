<template>
  <section id="sec_1">
    <div v-for="(photo, index) in photos"
    :key="index" class="img_cont">
      <img :src="photo.src" :alt="photo.alt" />
      <div class="hover_eye">ou</div>
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
    imgHovered(index) {
      this.imgHover = index;
    }
  }
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
  }
  img {
    width: 100%;
  }
  .hover_eye {
    padding: 1rem;
    background: red;
    border-radius: 50%;
    display: inline-block;
    position: absolute;
    z-index: 9;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
  }
}
.display_i_b {
  display: inline-block;
}
.display_none {
  display: none;
}
</style>
