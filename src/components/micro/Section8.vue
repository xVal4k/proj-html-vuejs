<template>
  <section id="sec_8">
    <div class="left_col_cont">
      <div class="left_col">
        <p class="above_title">MADE WITH LOVE</p>
        <h1>DELISH PIZZA DEALS</h1>
        <div class="list_events">
          <div v-for="event in events" :key="event" class="event">
            <div class="left">
              <p class="day">{{ event.day }}</p>
              <p class="month">{{ event.month }}</p>
            </div>
            <div class="right">
              <h3>{{ event.descr }}</h3>
              <p class="location">{{ event.location }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="right_col">
      <img src="../../assets/images/img/h3-img-5a.jpg" alt="" />
    </div>
  </section>
</template>

<script>
/* eslint-disable */

export default {
  name: "Section8",
  data() {
    return {
      events: [
        {
          day: "02",
          month: "NOV",
          descr: "TRADITIONAL NEAPOLITAN PIES IN KYOTO PIZZA MERCATO",
          location: "204 E. Pizzetta Tommaso",
        },
        {
          day: "03",
          month: "NOV",
          descr: "TERARAZZA PATIO DINING SPACE OPENING THIS WEEKEND",
          location: "204 E. Pizzetta Tommaso",
        },
        {
          day: "05",
          month: "NOV",
          descr: "SIENNA PRIVATE DINING ROOM WITH STEPHANE BRUNN",
          location: "204 E. Pizzetta Tommaso",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
#sec_8 {
  display: flex;
  margin: 0.5rem 0;
  .left_col_cont {
    width: 50%;
    background: black;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    border-bottom: solid 5rem white;
    .left_col {
      width: 50%;
      margin-left: -5rem;
    }
    .above_title {
      color: tomato;
      font-size: 10px;
      font-weight: bold;
    }
    h1 {
      margin: 0.5rem 0;
    }
    .list_events {
      display: flex;
      flex-direction: column;
      .event {
        display: flex;
        padding: 2rem 0;
        &:nth-child(2) {
          border-top: dotted 2px red;
          border-bottom: dotted 2px red;
        }
        .day {
          font-size: 2rem;
          font-weight: bold;
          color: tomato;
        }
        .month {
          font-weight: bold;
        }
        .right {
          margin-left: 2rem;
          .location {
            margin-top: .75rem;
            font-size: 10px;
            color: tomato;
          }
        }
      }
    }
  }
  .right_col {
    width: 50%;
    img {
      width: 100%;
    }
  }
}
</style>
