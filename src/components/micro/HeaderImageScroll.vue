<template>
  <div class="HdImgCont">
    <img
      v-for="(slice, index) in slices"
      :class="activeIndex == index ? 'display_block' : ''"
      :key="index"
      class="pizza_slice"
      :src="slice.src"
      :alt="slice.alt"
    />
    <img
      v-for="(bcktext, index) in text"
      :key="index"
      :class="activeIndex == index ? 'display_block' : ''"
      class="header_bck_text"
      :src="bcktext.src"
      :alt="bcktext.alt"
    />
    <button @click="previous" class="btn_prev">PREV</button>
    <button @click="next" class="btn_next">NEXT</button>
  </div>
</template>

<script>
/* eslint-disable */

import urbanSlice from "../../assets/images/img/h3-rev-img-6.png";
import urbanText from "../../assets/images/img/h3-rev-img-5.png";
import tasteSlice from "../../assets/images/img/h3-rev-img-4.png";
import tasteText from "../../assets/images/img/h3-rev-img-3.png";
import crustSlice from "../../assets/images/img/h3-rev-img-2.png";
import crustText from "../../assets/images/img/h3-rev-img-1.png";

export default {
  name: "HeaderImageScroll",
  components: {
    urbanSlice,
    urbanText,
    tasteSlice,
    tasteText,
    crustSlice,
    crustText,
  },
  data() {
    return {
      activeIndex: 0,
      slices: [
        {
          src: urbanSlice,
          alt: "urban slice",
        },
        {
          src: tasteSlice,
          alt: "taste slice",
        },
        {
          src: crustSlice,
          alt: "crust slice",
        },
      ],
      text: [
        {
          src: urbanText,
          alt: "urban text",
        },
        {
          src: tasteText,
          alt: "taste text",
        },
        {
          src: crustText,
          alt: "crust text",
        },
      ],
    };
  },
  methods: {
    next() {
      if (this.activeIndex == this.slices.length - 1) {
        this.activeIndex = 0;
      } else {
        this.activeIndex++;
      }
    },
    previous() {
      if (this.activeIndex == 0) {
        this.activeIndex = this.slices.length - 1;
      } else {
        this.activeIndex--;
      }
    },
  },
};
</script>

<style scoped lang="scss">
.HdImgCont {
  padding: 0.5rem 0 3rem 0;
  text-align: center;

  .pizza_slice {
    width: 15%;
    margin: 0 auto;
    position: relative;
    z-index: 9;
    display: none;
  }

  .header_bck_text {
    width: 40%;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    z-index: 0;
    display: none;
  }

  button {
    width: 60px;
    height: 30px;
    font-size: 8px;
    font-weight: bold;
    border-top-left-radius: 50px;
    border-top-right-radius: 50px;
    position: absolute;
    border: 2px solid transparent;
    background: white;
    color: #d2401e;
    cursor: pointer;
  }

  .btn_prev {
    left: -20px;
    top: 50%;
    transform: rotate(90deg);
  }

  .btn_next {
    right: -20px;
    top: 50%;
    transform: rotate(-90deg);
  }

  .display_block {
    display: block;
  }
}
</style>
