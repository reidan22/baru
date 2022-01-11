<template>
  <div id="main" class="">
    <b-row class="centrify">
      <span style="font-size: 20px; margin-bottom: 20px" class="text"
        >as of</span
      >
    </b-row>
    <b-row class="centrify date">
      <span>{{ today[0] }}</span>
    </b-row>
    <b-row class="centrify date">
      <span>{{ today[1] }}</span>
    </b-row>
    <b-row class="centrify">
      <span style="font-size: 20px; margin-top: 20px" class="text">{{
        message
      }}</span>
    </b-row>
    <b-row id="button" class="centrify">
      <div id="iconbutton" @click="onClickHeart()">
        <b-icon icon="heart-fill" id="icon"> </b-icon>
      </div>
    </b-row>
  </div>
</template>
<script>
let messages = [
  "i miss you!",
  "i miss you baruu!",
  "wuv youuu!",
  "wuv youuu baruuu!",
  "i wuv youuu!",
  "i wuv youuu baruu!",
  "i want you baruu!",
  "i want you!",
  "i wanna kiss you mwahhh!",
  "i wanna hug you!",
  "gihigugma tikaa!",
  "youre my baruuu!",
  "youre my wuvvv!",
  "gimingaw ko nimoo!",
  "i gotchuu my wuv!",
  "youre my favorite boy!",
  "can't wait to see you!",
  "my kokoro feels wavey when your name pops up!",
  "youre my sunflower!",
  "i want your warm hugss!",
  "i think about u all the time my baruu!",
];
export default {
  data() {
    return {
      today: null,
      isVisible: true,
      message: messages[Math.floor(Math.random() * messages.length)],
    };
  },
  mounted() {
    setInterval(() => {
      this.getTimeNow();
      // this.isVisible = !this.isVisible;
    }, 750);
  },
  methods: {
    onClickHeart() {
      this.message = messages[Math.floor(Math.random() * messages.length)];
    },
    getTimeNow() {
      const today = new Date();
      const date =
        today.getFullYear() +
        "/" +
        (today.getMonth() + 1) +
        "/" +
        today.getDate();
      const time =
        today.getHours() + ":" + String(today.getMinutes()).padStart(2, "0");
      this.secondsNow = today.getSeconds();
      this.today = [date, time + " PHT"];
    },
  },
  computed: {},
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css?family=Montserrat:900i&display=swap");

#main {
  font-size: 30px;
  font-family: "Montserrat", sans-serif;
}

#iconbutton {
  padding: 7px;
  color: rgb(75, 25, 190);
}

.date {
  font-size: 50px;
  letter-spacing: 2px;
  -webkit-text-fill-color: transparent;
  -webkit-text-stroke-width: 1px;
  -webkit-text-stroke-color: rgb(255, 255, 255);
  text-shadow: 2.5px 2.5px #ff1f8f, 7px 7px #000000;
}

.text {
  letter-spacing: 2px;
  -webkit-text-fill-color: transparent;
  -webkit-text-stroke-width: 0.5px;
  -webkit-text-stroke-color: rgb(255, 255, 255);
  text-shadow: 0px 0px #ff1f8f;
  width: 90vw;
}
</style>
