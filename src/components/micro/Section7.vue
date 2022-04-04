<template>
  <section id="sec_7">
    <div class="intro">
      <p class="above_title">CHOOSE YOUR FLAVOR</p>
      <h1>THE BEST PIZZA MENU IN TOWN</h1>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Id harum doloremque dolor, a
        recusandae nisi, quam eveniet sit
      </p>
    </div>
    <div class="pizza_list_cont">
      <div v-for="pizza in list" :key="pizza" class="pizza_list">
        <img :src="pizza.src" :alt="pizza.name" />
        <div class="pizza_infos">
          <p class="pizza_name">{{ pizza.name }}</p>
          <span class="old_price">{{ pizza.oldPrice }}</span>
          <span class="current_price">{{ pizza.currentPrice }}</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
/* eslint-disable */

import Bismarck from "../../assets/images/img/h3-product-img-1a-100x100.png";
import FioriZucca from "../../assets/images/img/h3-product-img-2a-150x150.png";
import Valdostana from "../../assets/images/img/h3-product-img-3a-150x150.png";
import Tartufata from "../../assets/images/img/h3-product-img-4a-150x150.png";
import Francescana from "../../assets/images/img/h3-product-img-5a-150x150.png";
import Campagnola from "../../assets/images/img/h3-product-img-6a-100x100.png";

export default {
  name: "Section7",
  data() {
    return {
      list: [
        {
          src: Bismarck,
          name: "BISMARCK",
          oldPrice: "$35.00",
          currentPrice: "$30.00",
        },
        {
          src: FioriZucca,
          name: "FIORI DI ZUCCA",
          currentPrice: "$7.00 - $50.00",
        },
        {
          src: Valdostana,
          name: "VALDOSTANA",
          currentPrice: "$55.00",
        },
        {
          src: Tartufata,
          name: "PIZZA TARTUFATA",
          currentPrice: "$45.00",
        },
        {
          src: Francescana,
          name: "FRANCESCANA",
          currentPrice: "$25.00",
        },
        {
          src: Campagnola,
          name: "CAMPAGNOLA",
          currentPrice: "$50.00 - $95.00",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
#sec_7 {
  text-align: center;
  padding: 5rem 0;
  .intro {
    width: 33%;
    margin: 0 auto 5rem;
    p {
      color: grey;
      font-size: 12px;
      font-weight: bold;
    }
    .above_title {
      color: tomato;
      font-size: 10px;
      font-weight: bold;
    }
    h1 {
      margin: .5rem 0 1rem 0;
    }
  }
  .pizza_list_cont {
    display: flex;
    flex-wrap: nowrap;
    .pizza_list {
      display: flex;
      flex-direction: column;
      width: 100%;
      margin: 0 3rem;
      .pizza_infos {
        margin: 1rem 0;
        .pizza_name {
          font-size: 14px;
          font-weight: bold;
          color: gold;
          margin-bottom: .25rem;
        }
        .old_price {
          font-size: 14px;
          font-weight: bold;
          margin: .25rem .5rem;
          color: grey;
          text-decoration: line-through;
        }
        .current_price {
          color: tomato;
          font-size: 14px;
          font-weight: bold;
        }
      }
    }
  }
}
</style>
