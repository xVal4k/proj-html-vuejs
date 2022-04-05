<template>
  <section id="sec_2">
    <h1>&ldquo;</h1>
    <div
      v-for="(post, index) in posts"
      :key="index"
      class="sec2_cont"
      :class="activeIndex == index ? 'display_block' : ''"
    >
      <p class="msg">"{{ post.msg }}"</p>
      <p class="post_date">{{ post.date }}</p>
    </div>
    <div
      v-for="(dot, index) in 3"
      :key="index"
      class="mini_dot"
      :class="activeIndex == index ? 'orange' : ''"
    ></div>
    <button @click="previous" class="btn_prev">PREV</button>
    <button @click="next" class="btn_next">NEXT</button>
    <svg xmlns="http://www.w3.org/2000/svg" width="15" viewBox="0 0 18 23"><g fill="#D2401E"><path d="M18 19.9c0-.1 0-.2-.1-.2 0-.1 0-.1-.1-.2 0-.1-.1-.3-.2-.6l-.3-.8c-.2-.4-.4-1.1-.6-1.5L10.4 1.2C10.3.8 9.9 0 9.1 0H9h-.1c-.8 0-1.2.8-1.3 1.2L1.3 16.6c-.2.4-.4 1.1-.6 1.5l-.3.8c-.1.3-.2.5-.2.6 0 .1-.1.1-.1.2s-.1.2-.1.3c-.1.3 0 .7.4 1.1.1 0 .1.1.2.1.1.1.3.2.5.3.2 0 2.8 1.5 7.6 1.5h.6c4.8 0 7.4-1.5 7.5-1.6.2-.1.4-.2.5-.3.1-.1.2-.1.2-.2.5-.3.5-.7.5-1zm-7.2-15l1 2.5c-.3.1-.6.2-.9 0-.3-.1-.6-.3-.8-.7-.1-.2-.2-.6-.1-.9.2-.4.4-.6.8-.9-.1.1 0 .1 0 0zM5.7 8.5c.7.4 1.3.9 1.6 1.6.3.7.3 1.6 0 2.3-.3.8-.9 1.3-1.6 1.7-.7.3-1.5.3-2.2 0l2.2-5.6zm-2.6 6.6c1 .4 2.1.4 3-.1 1-.4 1.8-1.2 2.2-2.2.4-1 .4-2.1 0-3.1-.5-1-1.2-1.7-2.2-2.1l2.4-6c.2-.3.3-.6.4-.6 0 .1.1.1.1.1s.1 0 .1-.1c.1 0 .2.2.4.6l1 2.4h-.2c-.6.3-1 .8-1.2 1.4-.3.6-.2 1.3.1 1.8.3.6.8 1 1.4 1.2.5.2 1.1.2 1.7-.1l3.5 8.6c.1.3.3.8.5 1.2h-.2c-.1 0-6.4 3.3-14.2 0h-.1c.2-.4.4-.9.5-1.2l.8-1.8zm13.2 5.4s-2.4 1.4-7 1.4h-.6c-4.6 0-7-1.4-7-1.4-.4-.2-.7-.4-.7-.4s.1-.3.3-.7l.1-.1.1.1c4.3 1.8 8.2 1.7 10.6 1.3 2.7-.4 4.4-1.3 4.4-1.4h.1l.1.1c.1.3.3.6.3.6 0 .1-.3.3-.7.5z"/><path d="M11.2 18.4c1.1 0 2-.9 2-2s-.9-2-2-2-2 .9-2 2c.1 1.1.9 2 2 2zm0-2.9c.5 0 .9.4.9.9s-.4.9-.9.9-.9-.4-.9-.9.4-.9.9-.9z"/></g></svg>
  </section>
</template>

<script>
/* eslint-disable */

export default {
  name: "Section2",
  data() {
    return {
      activeIndex: 0,
      posts: [
        {
          msg: "FORGET THE TRENDY PIZZA SHOPS, THIS HIDDEN SPOT MAKES THE BEST NEW YORK-STYLE PIZZA SLICE IN NAPLES.",
          date: "WASHINGTON POST 2018",
        },
        {
          msg: "FORGET THE TRENDY PIZZA SHOPS, REMEMBER THIS INSTEAD: WHATEVER THE QUESTION, PIZZA IS THE ANSWER.",
          date: "FUNNY POST 2022",
        },
        {
          msg: "MY LOVE IS PIZZA SHAPED. WON'T YOU HAVE A SLICE? IT'S CIRCULAR, SO THERE'S ENOUGH TO GO AROUND",
          date: "DORA J. AROD'S POST",
        },
      ],
    };
  },
  methods: {
    next() {
      if (this.activeIndex == this.posts.length - 1) {
        this.activeIndex = 0;
      } else {
        this.activeIndex++;
      }
    },
    previous() {
      if (this.activeIndex == 0) {
        this.activeIndex = this.posts.length - 1;
      } else {
        this.activeIndex--;
      }
    },
  },
};
</script>

<style scoped lang="scss">
#sec_2 {
  background-image: url(../../assets/images/img/h3-testimonials-bckgrnd.jpg);
  background-size: 80%;
  background-position: 2rem center;
  padding: 6rem 0;
  text-align: center;
  position: relative;
  margin-bottom: 0.5rem;
  letter-spacing: 2px;
  h1 {
    font-size: 8rem;
    margin: -4rem 0;
    color: #b7903c;
  }
  .sec2_cont {
    width: 50%;
    max-width: 800px;
    margin: 0 auto;
    font-weight: bold;
    display: none;
    .msg {
      font-size: 22px;
      line-height: 2rem;
      font-weight: bold;
    }
    .post_date {
      font-size: 10px;
      margin-top: 0.5rem;
      margin-bottom: 1rem;
      color: #d2401e;
    }
  }
  .mini_dot {
    width: 5px;
    height: 5px;
    display: inline-block;
    margin: 0 2px;
    border-radius: 50%;
    background: #00000026;
    border: solid 1px transparent;
  }
  button {
    width: 50px;
    height: 25px;
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
    left: -12.5px;
    top: 50%;
    transform: rotate(90deg);
  }

  .btn_next {
    right: -12.5px;
    top: 50%;
    transform: rotate(-90deg);
  }
  .display_block {
    display: block;
  }
  .orange {
    background: #b7903c;
  }
  svg {
    bottom: 25px;
  }
}
</style>
