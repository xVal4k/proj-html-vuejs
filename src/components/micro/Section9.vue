<template>
  <section id="sec_9">
    <div class="first_select_cont">
      <select name="groupSize" class="group_size">
        <option value="1">1 Person</option>
        <option value="2">2 People</option>
        <option value="3">3 People</option>
        <option value="4">4 People</option>
        <option value="5">5 People</option>
        <option value="6">6 People</option>
        <option value="7">7 People</option>
        <option value="8">8 People</option>
        <option value="9">9 People</option>
        <option value="10">10 People</option>
      </select>
      <p class="abs_text">* Powered by OpenTable</p>
    </div>
    <div class="mid_input">FOR</div>
    <label for="input_date">
      <input id="input_date" type="date"/>
    </label>
    <div class="mid_input">AT</div>
    <label for="input_hour">
      <input id="input_hour" type="time"/>
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
  margin: 0.5rem 0;
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
  select, input {
    cursor: pointer;
  }
  input,
  .group_size {
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
    background: #d2401e;
    border: solid 1px #d2401e;
    font-size: 10px;
    letter-spacing: 2px;
  }
  .first_select_cont {
    position: relative;
    .abs_text {
      position: absolute;
      left: 15px;
      bottom: -25px;
      color: white;
      font-size: 12px;
      opacity: 0.7;
    }
  }
}
</style>
