<template>
  <section id="sec_4">
    <div class="row row_top">
      <div class="col col_left"></div>
      <div class="col col_center"></div>
      <div class="col col_right"></div>
    </div>
    <div class="row row_middle">
      <div class="col col_left"></div>
      <div class="col col_center"></div>
      <div class="col col_right"></div>
    </div>
    <div class="row row_bottom">
      <div class="col col_left"></div>
      <div class="col col_center"></div>
      <div class="col col_right"></div>
    </div>
    <h1>
      GO AHEAD AND <br />
      BUILD YOUR <br />
      OWN PIZZA <br />
      WE WON'T <br>
      JUSTGE!
    </h1>
  </section>
</template>

<script>
/* eslint-disable */

export default {
  name: "Section4",
};
</script>

<style scoped lang="scss">
#sec_4 {
  margin: 0.5rem 0;
  position: relative;
  h1 {
    position: absolute;
    top: 50%;
    left: 20%;
    color: white;
    font-size: 3rem;
    transform: translateY(-50%);
  }
  .row {
    display: flex;
    .col {
      background-image: url(../../assets/images/img/h3-background-img.jpg);
      background-size: auto;
    }
    .col_left,
    .col_right {
      width: 6.7%;
      max-width: 128.64px;
    }
    .col_center {
      width: 86.6%;
      max-width: 1662.72px;
    }
  }
  .row_top,
  .row_bottom {
    .col_left,
    .col_right {
      &:before {
        content: "";
        float: left;
        padding-top: 100%;
      }
    }
  }
  .row_middle {
    .col_left,
    .col_right {
      &:before {
        content: "";
        float: left;
        padding-top: 230%;
      }
    }
  }
  .row_top {
    .col_left {
      background-position: 99% 100%;
    }
    .col_center {
      background-position: bottom;
      background-size: cover;
    }
    .col_right {
      background-position: 2% 100%;
    }
  }
  .row_middle {
    .col_left {
      background-position: 100% 4%;
    }
    .col_center {
      background-position: top right;
      background-size: cover;
    }
    .col_right {
      background-position: 2% 7%;
    }
  }
  .row_bottom {
    .col_left {
      background-position: 100% 65%;
    }
    .col_center {
      background-position: 40% 65%;
      background-size: cover;
    }
    .col_right {
      background-position: 0% 65%;
    }
  }
}
</style>
