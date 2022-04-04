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
  h1 {
    font-size: 8rem;
    margin: -4rem 0;
    color: #b7903c;
  }
  .sec2_cont {
    width: 40%;
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
      color: tomato;
    }
  }
  .mini_dot {
    width: 5px;
    height: 5px;
    display: inline-block;
    margin: 0 2px;
    border-radius: 50%;
    background: grey;
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
    background: orange;
  }
}
</style>
