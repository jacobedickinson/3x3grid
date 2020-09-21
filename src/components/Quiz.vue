<template>
  <div>
    <image
      src="https://www.kindpng.com/picc/m/8-88795_question-mark-png-transparent-background-question-marks-png.png"
      alt
    />
    <h1 style="color: red;3">Quiz Time!</h1>
    </image>
    <h4 class="q1">Question 1:</h4>
    <p class="q1">What Year was Battle of hastings?</p>
    <select v-model="answer1">
      <option>Year 1066</option>
      <option>Year 1099</option>
      <option>Year 2101</option>
      <option>Year 2010</option>
    </select>
    <br />
    <h4 class="q2">Question 2:</h4>
    <p class="q2">Best Drink?</p>
    <select v-model="answer2">
      <option>Tea</option>
      <option>Coffee</option>
      <option>Coke</option>
      <option>Water</option>
    </select>
    <br />
    <h4 class="q3">Question 3:</h4>
    <p class="q3">What Is Faster?</p>
    <select v-model="answer3">
      <option>Car</option>
      <option>Bike</option>
      <option>Horse</option>
      <option>Plane</option>
    </select>
    <br />
    <h4 class="q4">Question 4:</h4>
    <p class="q4">Warmest Clothing?</p>
    <select v-model="answer4">
      <option>Tshirt</option>
      <option>Hoody</option>
      <option>Coat</option>
      <option>Trousers</option>
    </select>
    <br />
    <br>
    <button v-on:click="checkAnswers()">Submit</button>
    <br> <br>
  </div>
</template>

<script>
export default {
  data() {
    return {
      answerA: "",
      answerB: "",
      answerC: "",
      answerD: "",
    };
  },
  methods: {
    // match answers to correct data and play sound
    checkAnswers: function () {
      if (
        this.answer1 == "Year 1066" &&
        this.answer2 == "Water" &&
        this.answer3 == "Plane" &&
        this.answer4 == "Coat"
      ) {
        alert("CORRECT");
        var sound = new Audio("3x3grid/src/assets/434111__nevermoire__aaah-yeete.mp3");
        sound.play();
      } else {
        alert("WRONG");
      }
    },
  },
};
</script>

<style scoped>
button{
  background-color: green;
  width: 4em;
}
div{
 background-image: url("https://www.kindpng.com/picc/m/8-88795_question-mark-png-transparent-background-question-marks-png.png");
 background-position: center;}
</style>

