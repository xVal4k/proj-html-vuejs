<template>
  <section id="sec_9">
    <label for="input_people">
      <input id="input_people" type="text" placeholder="1 Person" />
      <p class="abs_text">* Powered by OpenTable</p>
    </label>
    <div class="mid_input">FOR</div>
    <label for="input_date">
      <input id="input_date" type="date" placeholder="11/29/2020" />
    </label>
    <div class="mid_input">AT</div>
    <label for="input_hour">
      <input id="input_hour" type="time" placeholder="7.00 pm" />
    </label>
    <button>BOOK A TABLE</button>
  </section>
</template>

<script>
/* eslint-disable */

export default {
  name: "Section9",
};
</script>

<style scoped lang="scss">
#sec_9 {
  margin: .5rem 0;
  background-image: url(../../assets/images/img/h3-background-img-3.jpg);
  background-size: cover;
  background-position: center;
  padding: 3rem 0;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  label {
    position: relative;
  }
  input {
    margin: 0 1rem;
    padding: 0.75rem;
    width: 200px;
    height: 3rem;
    border: solid 1px transparent;
    font-size: 12px;
  }
  .mid_input {
    width: 2rem;
    text-align: center;
    font-size: 12px;
    font-weight: bold;
    color: white;
  }
  button {
    margin: 0 3rem;
    height: 3rem;
    padding: 0 3rem;
    cursor: pointer;
    color: white;
    background: tomato;
    border: solid 1px tomato;
  }
  .abs_text {
    position: absolute;
    left: 15px;
    bottom: -25px;
    color: white;
    font-size: 12px;
    opacity: .7;
  }
}
</style>
