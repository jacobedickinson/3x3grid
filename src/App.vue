<template>
  <div id="app">
    <Clock />
    <LogIn />
    <Quiz />
    <Delete />
    <Submit />
    <Shopping />
    <Search />
    <Restructure />
    <EightBall />
  </div>
</template>
<script>
import Clock from "@/components/Clock.vue";
import LogIn from "@/components/LogIn.vue";
import Delete from "@/components/Delete.vue";
import Search from "@/components/Search.vue";
import Submit from "@/components/Submit.vue";
import Shopping from "@/components/Shopping.vue";
import Quiz from "@/components/Quiz.vue";
import Restructure from "@/components/Restructure.vue";
import EightBall from "@/components/EightBall.vue";

export default {
  components: {
    Clock,
    LogIn,
    Delete,
    Search,
    Submit,
    Shopping,
    Quiz,
    Restructure,
    EightBall,
  },
};
</script>
<style scoped>
#app {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  text-align: center;
}
</style>
