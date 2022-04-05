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
        <div class="card_name">{{ photo.name }}</div>
        <p>{{ photo.role }}</p>
        <p>
          <i class="fab fa-instagram"></i>
          <i class="fab fa-twitter"></i>
          <i class="fab fa-facebook-f"></i>
        </p>
      </div>
    </div>
    <svg xmlns="http://www.w3.org/2000/svg" width="15" viewBox="0 0 18 23"><g fill="#D2401E"><path d="M18 19.9c0-.1 0-.2-.1-.2 0-.1 0-.1-.1-.2 0-.1-.1-.3-.2-.6l-.3-.8c-.2-.4-.4-1.1-.6-1.5L10.4 1.2C10.3.8 9.9 0 9.1 0H9h-.1c-.8 0-1.2.8-1.3 1.2L1.3 16.6c-.2.4-.4 1.1-.6 1.5l-.3.8c-.1.3-.2.5-.2.6 0 .1-.1.1-.1.2s-.1.2-.1.3c-.1.3 0 .7.4 1.1.1 0 .1.1.2.1.1.1.3.2.5.3.2 0 2.8 1.5 7.6 1.5h.6c4.8 0 7.4-1.5 7.5-1.6.2-.1.4-.2.5-.3.1-.1.2-.1.2-.2.5-.3.5-.7.5-1zm-7.2-15l1 2.5c-.3.1-.6.2-.9 0-.3-.1-.6-.3-.8-.7-.1-.2-.2-.6-.1-.9.2-.4.4-.6.8-.9-.1.1 0 .1 0 0zM5.7 8.5c.7.4 1.3.9 1.6 1.6.3.7.3 1.6 0 2.3-.3.8-.9 1.3-1.6 1.7-.7.3-1.5.3-2.2 0l2.2-5.6zm-2.6 6.6c1 .4 2.1.4 3-.1 1-.4 1.8-1.2 2.2-2.2.4-1 .4-2.1 0-3.1-.5-1-1.2-1.7-2.2-2.1l2.4-6c.2-.3.3-.6.4-.6 0 .1.1.1.1.1s.1 0 .1-.1c.1 0 .2.2.4.6l1 2.4h-.2c-.6.3-1 .8-1.2 1.4-.3.6-.2 1.3.1 1.8.3.6.8 1 1.4 1.2.5.2 1.1.2 1.7-.1l3.5 8.6c.1.3.3.8.5 1.2h-.2c-.1 0-6.4 3.3-14.2 0h-.1c.2-.4.4-.9.5-1.2l.8-1.8zm13.2 5.4s-2.4 1.4-7 1.4h-.6c-4.6 0-7-1.4-7-1.4-.4-.2-.7-.4-.7-.4s.1-.3.3-.7l.1-.1.1.1c4.3 1.8 8.2 1.7 10.6 1.3 2.7-.4 4.4-1.3 4.4-1.4h.1l.1.1c.1.3.3.6.3.6 0 .1-.3.3-.7.5z"/><path d="M11.2 18.4c1.1 0 2-.9 2-2s-.9-2-2-2-2 .9-2 2c.1 1.1.9 2 2 2zm0-2.9c.5 0 .9.4.9.9s-.4.9-.9.9-.9-.4-.9-.9.4-.9.9-.9z"/></g></svg>
  </section>
</template>

<script>
/* eslint-disable */
import Mike from "../../assets/images/img/h1-team-1a-700x700.jpg";
import Sara from "../../assets/images/img/h1-team-2a.jpg";
import Jimmy from "../../assets/images/img/h1-team-4a.jpg";
import Gloria from "../../assets/images/img/h1-team-3a.jpg";

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
  position: relative;
  .img_cont {
    position: relative;
    width: calc(100% / 4);
    background-image: radial-gradient(lightgrey 10%, transparent 11%),
    radial-gradient(#fff 10%, transparent 11%);
    background-size: 10px 10px;
    background-position: 0 0, 30px 30px;
    background-repeat: repeat;
    letter-spacing: 1px;
    img {
      width: 100%;
      position: relative;
      z-index: 9;
    }

    .hover_info {
      width: 90%;
      height: 90%;
      background: #D2401E;
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
      .card_name {
      font-size: 30px;
      }
      p {
        font-size: 14px;
        margin: 0.25rem 0 0.5rem 0;
      }
      .fab {
        margin: 0 .5rem;
        cursor: pointer;
      }
    }
  }
  .display_none {
    display: none;
  }
  svg {
    bottom: 40px;
  }
}
</style>
