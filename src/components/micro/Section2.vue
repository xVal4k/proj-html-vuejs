<template>
  <section id="sec_2">
    <div v-for="post in posts" :key="post" class="sec2_cont">
      <h1>&ldquo;</h1>
      <p class="msg">"{{ post.msg }}"</p>
      <p class="post_date">{{ post.date }}</p>
    </div>
    <div class="mini_dot"></div>
    <div class="mini_dot"></div>
    <div class="mini_dot"></div>
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
      posts: [
        {
          msg: "FORGET THE TRENDY PIZZA SHOPS, THIS HIDDEN SPOT MAKES THE BEST NEW YORK-STYLE PIZZA SLICE IN NAPLES",
          date: "WASHINGTON POST 2018",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
#sec_2 {
  background-image: url(../../assets/images/img/h3-testimonials-bckgrnd.jpg);
  background-size: 80%;
  background-position: 2rem center;
  padding: 4rem 0;
  text-align: center;
  position: relative;
  margin-bottom: .5rem;
  .sec2_cont {
    width: 40%;
    max-width: 800px;
    margin: 0 auto;
    font-weight: bold;
    h1 {
      font-size: 8rem;
      margin-bottom: -4rem;
      color: #b7903c;
    }
    .msg {
      line-height: 1.5rem;
      font-weight: bold;
    }
    .post_date {
      font-size: 10px;
      margin-top: .5rem;
      margin-bottom: 1rem;
    }
  }
  .mini_dot {
    width: 5px;
    height: 5px;
    display: inline-block;
    margin: 0 2px;
    border-radius: 50%;
    background: black;
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
}
</style>
