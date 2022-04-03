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
    padding: 10rem;
    font-weight: bold;
    position: relative;
    .cont {
      width: 80%;
      h1,
      h3 {
        margin-bottom: 0.5rem;
      }
      .red_price {
        color: red;
      }
      .grey_descr {
        margin-bottom: 1rem;
        font-size: 12px;
        line-height: 1rem;
        color: grey;
      }
      .item_descr {
        margin-left: 2.5rem;
      }
    }
  }
}
</style>
