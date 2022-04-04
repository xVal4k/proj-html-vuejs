<template>
  <nav>
    <div>
      <button>ORDER ONLINE</button>
    </div>
    <div class="center">
      <div class="center-left">
        <a href="#!" v-for="el in navbarCenterLeft" :key="el">{{ el }}</a>
      </div>
      <img src="../../assets/images/img/h5-logo-divided-header.png" alt="logo" />
      <div class="center-right">
        <a href="#!" v-for="el in navbarCenterRight" :key="el">{{ el }}</a>
      </div>
    </div>
    <div class="right">
      <a href="#!" v-for="el in navbarRight" :key="el">{{ el }}</a>
    </div>
  </nav>
</template>

<script>
/* eslint-disable */
export default {
  name: "NavBar",
  data() {
    return {
      navbarCenterLeft: ["HOME", "PAGES", "MENU"],
      navbarCenterRight: ["EVENT", "BLOG", "LANDING"],
      navbarRight: ["CART", "SEARCH"],
    };
  },
};
</script>

<style scoped lang="scss">
nav {
  width: 60%;
  max-width: 1000px;
  margin: 0 auto;
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding: 1rem;

  button {
    padding: 0.75rem 1.5rem;
    font-size: 10px;
    background: #d2401e;
    color: white;
    border: solid 1px #d2401e;
    cursor: pointer;
    font-family: 'Oswald', sans-serif;
  }

  a {
    color: white;
    text-decoration: none;
    padding: 1rem;
    font-size: 10px;
  }

  .center {
    display: flex;
    justify-content: center;
    align-items: center;
    img {
      width: 7rem;
      margin: 0 1rem;
    }
  }
}
</style>
