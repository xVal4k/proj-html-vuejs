<template>
  <footer>
    <div class="left_col">
      <div class="container">
        <div class="left_cont">
          <h5>FIND OUR RESTAURANTS</h5>
          <div v-for="restaurant in restaurants" :key="restaurant" class="restaurants">
            <p>{{ restaurant.str }}</p>
            <p>{{ restaurant.city }}</p>
            <p>{{ restaurant.tel }}</p>
          </div>
        </div>
        <div class="center_cont">
          <h5>WORKING HOURS</h5>
          <div v-for="item in workHours" :key="item" class="work_hours">
            <h6>{{ item.day }}</h6>
            <p>{{ item.time }}</p>
          </div>
          <h6>FOLLOW US: logo logo logo logo</h6>
        </div>
        <h4>
          THE DON PEPPE CREW <br />
          FIRST AND FOREMOST <br />
          VALUES IN AUTHENTIC, <br />
          WELL BAKED SLICE OF <br />
          PIZZA
        </h4>
      </div>
      <p class="credits">Created with &#10084; by <span class="green">Qode interactive</span></p>
    </div>
    <div class="right_col">
      <img src="../assets/images/img/footer-img-1.jpg" alt="bck img" />
    </div>
  </footer>
</template>

<script>
/* eslint-disable */

export default {
  name: "FooterPizza",
  data() {
    return {
      restaurants: [
        {
          str: "1614 E. Bell Rd #104",
          city: "Salerno, AZ 85022",
          tel: "(602)867-1010",
        },
        {
          str: "204 E. Pizzetta Tommaso",
          city: "Sorrento, AZ 85022",
          tel: "(358)867-1010",
        },
        {
          str: "Vale Puglia 54",
          city: "Torre Del Greco, AZ 85022",
          tel: "(359)867-1010",
        },
        {
          str: "Corso Itali AA",
          city: "Naples, AZ 85022",
          tel: "(989)867-1010",
        },
      ],
      workHours: [
        {
          day: "MONDAY",
          time: "Kitchen Closed",
        },
        {
          day: "TUESDAY UNTIL FRIDAY",
          time: "9.00 - 22.00",
        },
        {
          day: "SATURDAY",
          time: "Saturday 11am to midnight",
        },
        {
          day: "SUNDAY",
          time: "9.00 - 22.00",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
footer {
  display: flex;
  background: black;
  .left_col,
  .right_col {
    width: 50%;
  }
  .left_col {
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    padding: 4rem 4rem;
    .container {
      display: flex;
      justify-content: space-between;
      padding: 4rem 0;
      color: white;
      .work_hours {
        margin: 1rem 0;
        &:nth-child(2) p:last-child {
          color: tomato;
        }
      }
      h4 {
        line-height: 1.5rem;
      }
      h5,
      h6 {
        color: orange;
      }
      .restaurants {
        margin: 1rem 0;
      }
      p {
        color: grey;
        font-size: 12px;
        line-height: 1.2rem;
      }
    }
    .credits {
      color: orange;
      .green {
        color: green;
      }
    }
  }
  .right_col {
    img {
      width: 100%;
    }
  }
}
</style>
