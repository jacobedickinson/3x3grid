<template>
  <div>
    <div class="clock">
      <div class="clockbody">
        <h1>{{hrs}}:{{min}}:{{secs}}</h1>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  data() {
    return {
      hrs: "",
      min: "",
      secs: "",
    };
  },
  mounted() {
    setInterval(this.getTime, 1000);
  },
  methods: {
    getTime() {
      const today = new Date();
      this.hrs = today.getHours();
      this.min = today.getMinutes();
      if (this.min < 10) {
        this.min = "0" + this.min;
      }
      this.secs = today.getSeconds();
      if (this.secs < 10) {
        this.secs = "0" + this.secs;
      }
    },
  },
};
</script>

<style scoped>
.clockbody {
  border: black 2px solid;
  border-radius: 25px;
  background: grey;
  padding: 20px;
  width: 70%;
  height: 70%;
}
.clock {
  border-radius: 25px;
  background: #73ad21;
  padding: 20px;
  width: 100%;
  height: 100%;
}

p {
  text-decoration: blueviolet;
}
div {
  margin: auto;
}
</style>