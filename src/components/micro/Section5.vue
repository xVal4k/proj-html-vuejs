<template>
  <section id="sec_5">
    <div
      v-for="(photo, index) in workers"
      :key="index"
      @mouseover="setHover(index)"
      @mouseout="imgHover = null"
      @focus="setHover(index)"
      @focusout="imgHover = null"
      class="img_cont"
    >
      <img :src="photo.src" :alt="photo.name" :class="imgHover == index ? 'display_none' : ''"/>
      <div class="hover_info">
        <h2>{{ photo.name }}</h2>
        <p>{{ photo.role }}</p>
        <p>logo logo logo</p>
      </div>
    </div>
  </section>
</template>

<script>
/* eslint-disable */
import Mike from "../../assets/images/img/h1-team-1a-700x700.jpg";
import Sara from "../../assets/images/img/h1-team-2a.jpg";
import Jimmy from "../../assets/images/img/h1-team-3a.jpg";
import Gloria from "../../assets/images/img/h1-team-4a.jpg";

export default {
  name: "Section5",
  data() {
    return {
      workers: [
        {
          name: "Mike Garcia",
          role: "Head Chef",
          src: Mike,
        },
        {
          name: "Sara Smith",
          role: "Kitchen Porter",
          src: Sara,
        },
        {
          name: "Jimmy Martinez",
          role: "Chef",
          src: Jimmy,
        },
        {
          name: "Gloria Rodriguez",
          role: "Kitchen Porter",
          src: Gloria,
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
#sec_5 {
  margin: 0.5rem 0;
  display: flex;
  .img_cont {
    position: relative;
    width: calc(100% / 4);
    background-image: radial-gradient(lightgrey 10%, transparent 11%),
    radial-gradient(#fff 10%, transparent 11%);
    background-size: 10px 10px;
    background-position: 0 0, 30px 30px;
    background-repeat: repeat;
  }
  img {
    width: 100%;
    position: relative;
    z-index: 9;
  }
  .hover_info {
    width: 90%;
    height: 90%;
    background: tomato;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: white;
    position: absolute;
    z-index: 0;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    p {
      font-size: 14px;
      margin: 0.25rem 0 0.5rem 0;
    }
  }
  .display_none {
    display: none;
  }
}
</style>
