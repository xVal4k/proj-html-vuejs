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
      <svg xmlns="http://www.w3.org/2000/svg" width="15" viewBox="0 0 18 23"><g fill="#D2401E"><path d="M18 19.9c0-.1 0-.2-.1-.2 0-.1 0-.1-.1-.2 0-.1-.1-.3-.2-.6l-.3-.8c-.2-.4-.4-1.1-.6-1.5L10.4 1.2C10.3.8 9.9 0 9.1 0H9h-.1c-.8 0-1.2.8-1.3 1.2L1.3 16.6c-.2.4-.4 1.1-.6 1.5l-.3.8c-.1.3-.2.5-.2.6 0 .1-.1.1-.1.2s-.1.2-.1.3c-.1.3 0 .7.4 1.1.1 0 .1.1.2.1.1.1.3.2.5.3.2 0 2.8 1.5 7.6 1.5h.6c4.8 0 7.4-1.5 7.5-1.6.2-.1.4-.2.5-.3.1-.1.2-.1.2-.2.5-.3.5-.7.5-1zm-7.2-15l1 2.5c-.3.1-.6.2-.9 0-.3-.1-.6-.3-.8-.7-.1-.2-.2-.6-.1-.9.2-.4.4-.6.8-.9-.1.1 0 .1 0 0zM5.7 8.5c.7.4 1.3.9 1.6 1.6.3.7.3 1.6 0 2.3-.3.8-.9 1.3-1.6 1.7-.7.3-1.5.3-2.2 0l2.2-5.6zm-2.6 6.6c1 .4 2.1.4 3-.1 1-.4 1.8-1.2 2.2-2.2.4-1 .4-2.1 0-3.1-.5-1-1.2-1.7-2.2-2.1l2.4-6c.2-.3.3-.6.4-.6 0 .1.1.1.1.1s.1 0 .1-.1c.1 0 .2.2.4.6l1 2.4h-.2c-.6.3-1 .8-1.2 1.4-.3.6-.2 1.3.1 1.8.3.6.8 1 1.4 1.2.5.2 1.1.2 1.7-.1l3.5 8.6c.1.3.3.8.5 1.2h-.2c-.1 0-6.4 3.3-14.2 0h-.1c.2-.4.4-.9.5-1.2l.8-1.8zm13.2 5.4s-2.4 1.4-7 1.4h-.6c-4.6 0-7-1.4-7-1.4-.4-.2-.7-.4-.7-.4s.1-.3.3-.7l.1-.1.1.1c4.3 1.8 8.2 1.7 10.6 1.3 2.7-.4 4.4-1.3 4.4-1.4h.1l.1.1c.1.3.3.6.3.6 0 .1-.3.3-.7.5z"/><path d="M11.2 18.4c1.1 0 2-.9 2-2s-.9-2-2-2-2 .9-2 2c.1 1.1.9 2 2 2zm0-2.9c.5 0 .9.4.9.9s-.4.9-.9.9-.9-.4-.9-.9.4-.9.9-.9z"/></g></svg>
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
  background: url(https://donpeppe.qodeinteractive.com/wp-content/uploads/2019/10/h3-rev-bckgrnd-ing.jpg);
  .left_col,
  .right_col {
    width: 50%;
  }
  .left_col {
    display: flex;
    justify-content: space-between;
    flex-direction: column;
    padding: 3rem;
    .container {
      display: flex;
      justify-content: space-between;
      padding: 4rem 0;
      padding-right: 6rem;
      color: white;
      .work_hours {
        margin: 1rem 0;
        &:nth-child(2) p:last-child {
          color: #ab4027;
        }
        &:nth-child(4) h6:first-child:after {
          content: '*';
          color: #ab4027;
          font-size: 14px;
          margin: 2px;
        }
      }
      h4 {
        line-height: 1.5rem;
        font-size: 1rem;
        letter-spacing: .75px;
        font-weight: 500;
      }
      h5,
      h6 {
        color: #b7903c;
        letter-spacing: .2px;
      }
      .restaurants {
        margin: 1rem 0;
      }
      p {
        color: #8F8F8F;
        font-size: 10px;
        line-height: 1.2rem;
        letter-spacing: .7px;
      }
    }
    .credits {
      color: #b7903c;
      font-size: 9px;
      letter-spacing: 1.5px;
      .green {
        color: #339966;
      }
    }
  }
  .right_col {
    background-image: url(../assets/images/img/footer-img-1.jpg);
    background-position: center;
    background-size: cover;
    position: relative;
    svg {
      bottom: 25px;
    }
  }

}
</style>
