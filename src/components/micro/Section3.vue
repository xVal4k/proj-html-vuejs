<template>
  <section id="sec_3">
    <div class="left_col">
      <img
        class="small_img"
        src="../../assets/images/img/h1-img-7n.png"
        alt="pizza specials logo"
      />
    </div>
    <div class="right_col">
      <div class="cont">
        <h1>SPECIALS*</h1>
        <p class="grey_descr">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesent ut.
        </p>
        <div v-for="item in specials" :key="item" class="specials_items">
          <h3>
            <span class="red_price">${{ item.cost }}</span>
            {{ item.name }}
          </h3>
          <p class="item_descr grey_descr">{{ item.descr }}</p>
        </div>
        <svg xmlns="http://www.w3.org/2000/svg" width="15" viewBox="0 0 18 23"><g fill="#D2401E"><path d="M18 19.9c0-.1 0-.2-.1-.2 0-.1 0-.1-.1-.2 0-.1-.1-.3-.2-.6l-.3-.8c-.2-.4-.4-1.1-.6-1.5L10.4 1.2C10.3.8 9.9 0 9.1 0H9h-.1c-.8 0-1.2.8-1.3 1.2L1.3 16.6c-.2.4-.4 1.1-.6 1.5l-.3.8c-.1.3-.2.5-.2.6 0 .1-.1.1-.1.2s-.1.2-.1.3c-.1.3 0 .7.4 1.1.1 0 .1.1.2.1.1.1.3.2.5.3.2 0 2.8 1.5 7.6 1.5h.6c4.8 0 7.4-1.5 7.5-1.6.2-.1.4-.2.5-.3.1-.1.2-.1.2-.2.5-.3.5-.7.5-1zm-7.2-15l1 2.5c-.3.1-.6.2-.9 0-.3-.1-.6-.3-.8-.7-.1-.2-.2-.6-.1-.9.2-.4.4-.6.8-.9-.1.1 0 .1 0 0zM5.7 8.5c.7.4 1.3.9 1.6 1.6.3.7.3 1.6 0 2.3-.3.8-.9 1.3-1.6 1.7-.7.3-1.5.3-2.2 0l2.2-5.6zm-2.6 6.6c1 .4 2.1.4 3-.1 1-.4 1.8-1.2 2.2-2.2.4-1 .4-2.1 0-3.1-.5-1-1.2-1.7-2.2-2.1l2.4-6c.2-.3.3-.6.4-.6 0 .1.1.1.1.1s.1 0 .1-.1c.1 0 .2.2.4.6l1 2.4h-.2c-.6.3-1 .8-1.2 1.4-.3.6-.2 1.3.1 1.8.3.6.8 1 1.4 1.2.5.2 1.1.2 1.7-.1l3.5 8.6c.1.3.3.8.5 1.2h-.2c-.1 0-6.4 3.3-14.2 0h-.1c.2-.4.4-.9.5-1.2l.8-1.8zm13.2 5.4s-2.4 1.4-7 1.4h-.6c-4.6 0-7-1.4-7-1.4-.4-.2-.7-.4-.7-.4s.1-.3.3-.7l.1-.1.1.1c4.3 1.8 8.2 1.7 10.6 1.3 2.7-.4 4.4-1.3 4.4-1.4h.1l.1.1c.1.3.3.6.3.6 0 .1-.3.3-.7.5z"/><path d="M11.2 18.4c1.1 0 2-.9 2-2s-.9-2-2-2-2 .9-2 2c.1 1.1.9 2 2 2zm0-2.9c.5 0 .9.4.9.9s-.4.9-.9.9-.9-.4-.9-.9.4-.9.9-.9z"/></g></svg>
      </div>
    </div>
  </section>
</template>

<script>
/* eslint-disable */

export default {
  name: "Section3",
  data() {
    return {
      specials: [
        {
          cost: 10,
          name: "COMBO PICCOLO",
          descr:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesent ut aliquam dui.",
        },
        {
          cost: 20,
          name: "COMBO MEZZO",
          descr:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesent ut aliquam dui.",
        },
        {
          cost: 30,
          name: "COMBO GRANDE",
          descr:
            "Lorem ipsum dolor sit amet, consectetur adipisicing elit. Praesent ut aliquam dui.",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
#sec_3 {
  display: flex;

  .left_col,
  .right_col {
    width: calc(100% / 2);
    position: relative;
  }

  .left_col {
    background-image: url(../../assets/images/img/h1-img-4.jpg);
    background-position: center;
    background-size: cover;
    .big_img {
      width: 100%;
      z-index: 0;
    }
    .small_img {
      width: 40%;
      position: absolute;
      z-index: 9;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }
  }

  .right_col {
    padding: 8rem;
    position: relative;
    .cont {
      width: 70%;
      margin: 0 auto;
      h1 {
        font-size: 26px;
      }
      h1,
      h3 {
        margin-bottom: 0.5rem;
      }
      .red_price {
        color: #ab4027;
        margin-right: 0.5rem;
      }
      .grey_descr {
        margin-bottom: 1rem;
        font-size: 12px;
        line-height: 1.2rem;
        color: #8f8f8f;
        font-family: Arial, Helvetica, sans-serif;
        letter-spacing: 0.5px;
        font-weight: 400;
      }
      .item_descr {
        margin-left: 2.7rem;
        font-size: 10px;
      }
      svg {
        bottom: 22%;
      }
    }
  }
}
</style>
