<template>
  <section id="sec_5">
    <div v-for="(photo, index) in workers"
    :key="index" class="img_cont">
      <img :src="photo.src" :alt="photo.name" />
      <div class="hover_eye">
        <h2>{{ photo.name }}</h2>
        <p>{{ photo.role }}</p>
        <p>logo logo logo</p>
      </div>
    </div>
  </section>
</template>

<script>
/* eslint-disable */
import Mike from "../../assets/images/img/h1-team-1a-700x700.jpg";
import Sara from "../../assets/images/img/h1-team-2a.jpg";
import Jimmy from "../../assets/images/img/h1-team-3a.jpg";
import Gloria from "../../assets/images/img/h1-team-4a.jpg";

export default {
  name: 'Section5',
  data() {
    return {
      workers: [
        {
          name: 'Mike Garcia',
          role: 'Head Chef',
          src: Mike,
        },
        {
          name: 'Sara Smith',
          role: 'Kitchen Porter',
          src: Sara,
        },
        {
          name: 'Jimmy Martinez',
          role: 'Chef',
          src: Jimmy,
        },
        {
          name: 'Gloria Rodriguez',
          role: 'Kitchen Porter',
          src: Gloria,
        },
      ],
      imgHover: null,
    };
  },
}
</script>

<style scoped lang="scss">
#sec_5 {
  margin: .5rem 0;
  display: flex;
  .img_cont {
    position: relative;
    width: calc(100% / 4);
  }
  img {
    width: 100%;
  }
  .hover_eye {
    width: 90%;
    height: 90%;
    background: tomato;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: white;
    position: absolute;
    z-index: 9;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    p {
      font-size: 14px;
      margin: .25rem 0 .5rem 0;
    }
  }
}
</style>
