<template>
  <div class="hello">
    <h1>Timer</h1>
    <h1>{{seconds}}</h1>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data: () => ({
    seconds: 500,
  }),
  mounted() {
    console.log("mounted");
    this.updateTimer();
  },
  methods: {
    updateTimer() {
      const timer = setInterval(() => {
        if (this._seconds === 100) {
          clearInterval(timer);
          return;
        }
        // console.log(this.seconds);
        this.seconds--;
      }, 1000);
    },
  },
};
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
