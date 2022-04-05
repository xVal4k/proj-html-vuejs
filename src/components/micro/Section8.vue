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
              <div>{{ event.descr }}</div>
              <p class="location"><i class="fas fa-map-marker-alt"></i> {{ event.location }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="right_col">
      <img src="../../assets/images/img/h3-img-5a.jpg" alt="" />
      <svg class="svg_top" xmlns="http://www.w3.org/2000/svg" width="15" viewBox="0 0 18 23"><g fill="#D2401E"><path d="M18 19.9c0-.1 0-.2-.1-.2 0-.1 0-.1-.1-.2 0-.1-.1-.3-.2-.6l-.3-.8c-.2-.4-.4-1.1-.6-1.5L10.4 1.2C10.3.8 9.9 0 9.1 0H9h-.1c-.8 0-1.2.8-1.3 1.2L1.3 16.6c-.2.4-.4 1.1-.6 1.5l-.3.8c-.1.3-.2.5-.2.6 0 .1-.1.1-.1.2s-.1.2-.1.3c-.1.3 0 .7.4 1.1.1 0 .1.1.2.1.1.1.3.2.5.3.2 0 2.8 1.5 7.6 1.5h.6c4.8 0 7.4-1.5 7.5-1.6.2-.1.4-.2.5-.3.1-.1.2-.1.2-.2.5-.3.5-.7.5-1zm-7.2-15l1 2.5c-.3.1-.6.2-.9 0-.3-.1-.6-.3-.8-.7-.1-.2-.2-.6-.1-.9.2-.4.4-.6.8-.9-.1.1 0 .1 0 0zM5.7 8.5c.7.4 1.3.9 1.6 1.6.3.7.3 1.6 0 2.3-.3.8-.9 1.3-1.6 1.7-.7.3-1.5.3-2.2 0l2.2-5.6zm-2.6 6.6c1 .4 2.1.4 3-.1 1-.4 1.8-1.2 2.2-2.2.4-1 .4-2.1 0-3.1-.5-1-1.2-1.7-2.2-2.1l2.4-6c.2-.3.3-.6.4-.6 0 .1.1.1.1.1s.1 0 .1-.1c.1 0 .2.2.4.6l1 2.4h-.2c-.6.3-1 .8-1.2 1.4-.3.6-.2 1.3.1 1.8.3.6.8 1 1.4 1.2.5.2 1.1.2 1.7-.1l3.5 8.6c.1.3.3.8.5 1.2h-.2c-.1 0-6.4 3.3-14.2 0h-.1c.2-.4.4-.9.5-1.2l.8-1.8zm13.2 5.4s-2.4 1.4-7 1.4h-.6c-4.6 0-7-1.4-7-1.4-.4-.2-.7-.4-.7-.4s.1-.3.3-.7l.1-.1.1.1c4.3 1.8 8.2 1.7 10.6 1.3 2.7-.4 4.4-1.3 4.4-1.4h.1l.1.1c.1.3.3.6.3.6 0 .1-.3.3-.7.5z"/><path d="M11.2 18.4c1.1 0 2-.9 2-2s-.9-2-2-2-2 .9-2 2c.1 1.1.9 2 2 2zm0-2.9c.5 0 .9.4.9.9s-.4.9-.9.9-.9-.4-.9-.9.4-.9.9-.9z"/></g></svg>
      <svg xmlns="http://www.w3.org/2000/svg" width="15" viewBox="0 0 18 23"><g fill="#D2401E"><path d="M18 19.9c0-.1 0-.2-.1-.2 0-.1 0-.1-.1-.2 0-.1-.1-.3-.2-.6l-.3-.8c-.2-.4-.4-1.1-.6-1.5L10.4 1.2C10.3.8 9.9 0 9.1 0H9h-.1c-.8 0-1.2.8-1.3 1.2L1.3 16.6c-.2.4-.4 1.1-.6 1.5l-.3.8c-.1.3-.2.5-.2.6 0 .1-.1.1-.1.2s-.1.2-.1.3c-.1.3 0 .7.4 1.1.1 0 .1.1.2.1.1.1.3.2.5.3.2 0 2.8 1.5 7.6 1.5h.6c4.8 0 7.4-1.5 7.5-1.6.2-.1.4-.2.5-.3.1-.1.2-.1.2-.2.5-.3.5-.7.5-1zm-7.2-15l1 2.5c-.3.1-.6.2-.9 0-.3-.1-.6-.3-.8-.7-.1-.2-.2-.6-.1-.9.2-.4.4-.6.8-.9-.1.1 0 .1 0 0zM5.7 8.5c.7.4 1.3.9 1.6 1.6.3.7.3 1.6 0 2.3-.3.8-.9 1.3-1.6 1.7-.7.3-1.5.3-2.2 0l2.2-5.6zm-2.6 6.6c1 .4 2.1.4 3-.1 1-.4 1.8-1.2 2.2-2.2.4-1 .4-2.1 0-3.1-.5-1-1.2-1.7-2.2-2.1l2.4-6c.2-.3.3-.6.4-.6 0 .1.1.1.1.1s.1 0 .1-.1c.1 0 .2.2.4.6l1 2.4h-.2c-.6.3-1 .8-1.2 1.4-.3.6-.2 1.3.1 1.8.3.6.8 1 1.4 1.2.5.2 1.1.2 1.7-.1l3.5 8.6c.1.3.3.8.5 1.2h-.2c-.1 0-6.4 3.3-14.2 0h-.1c.2-.4.4-.9.5-1.2l.8-1.8zm13.2 5.4s-2.4 1.4-7 1.4h-.6c-4.6 0-7-1.4-7-1.4-.4-.2-.7-.4-.7-.4s.1-.3.3-.7l.1-.1.1.1c4.3 1.8 8.2 1.7 10.6 1.3 2.7-.4 4.4-1.3 4.4-1.4h.1l.1.1c.1.3.3.6.3.6 0 .1-.3.3-.7.5z"/><path d="M11.2 18.4c1.1 0 2-.9 2-2s-.9-2-2-2-2 .9-2 2c.1 1.1.9 2 2 2zm0-2.9c.5 0 .9.4.9.9s-.4.9-.9.9-.9-.4-.9-.9.4-.9.9-.9z"/></g></svg>
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
  letter-spacing: 1px;
  .left_col_cont {
    width: 50%;
    background: url(https://donpeppe.qodeinteractive.com/wp-content/uploads/2019/10/h3-rev-bckgrnd-ing.jpg);
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
      color: #AB4027;
      font-size: 10px;
      font-weight: bold;
      letter-spacing: 1.5px;
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
        justify-content: center;
        align-items: center;
        &:nth-child(2) {
          border-top: dotted 2px #B7903C;
          border-bottom: dotted 2px #B7903C;
        }
        .left {
          .day {
            font-size: 2.5rem;
            font-weight: bold;
            color: #AB4027;
          }
          .month {
            font-weight: bold;
            text-align: center;
            font-size: 20px;
            margin-top: -.75rem;
          }
        }
        .right {
          margin-left: 2rem;
          .location {
            margin-top: .75rem;
            font-size: 8px;
            color: #AB4027;
            .fas {
              margin-right: .5rem;
            }
          }
        }
      }
    }
  }
  .right_col {
    width: 50%;
    position: relative;
    .svg_top {
      top: 10px;
    }
    svg:last-child {
      bottom: 25%;
    }
    img {
      width: 100%;
    }
  }
}
</style>
