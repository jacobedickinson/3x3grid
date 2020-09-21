<template>
  <div class="eightball">
    <div class="container">
      <br />
      <br />
      <h3 style="color: grey
    ">{{answer}}</h3>
    </div>
    <input class="questionBox" v-model="inputBox" placeholder="What is your question?" />
    <br />
    <button class="askButton" v-on:click="whatsMyAnswer()">Ask!</button>
    <br />
  </div>
</template>


<script>
export default {
  data() {
    return {
      answer: "",
      inputBox: "",
      answers: [
        "Yes sir",
        "No way",
        "Absolutely right",
        "Absolutely Not",
        "Maybe",
        "Possibly",
        "Never",
        "50% Chance",
        "100% Chance",
        "Small Chance",
        "Large Chance",
        "100% Sure",
      ],
    };
  },
  methods: {
    whatsMyAnswer: function () {
      if (this.inputBox === "") {
        this.answer = "Please ask me a question";
      } else {
        this.inputBox = "";
        var randomNum = Math.floor(Math.random() * 10);
        this.answer = this.answers[randomNum];
      }
    },
  },
};
</script>

<style>
.eightball {
  background-image: url("https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcQhdrlkGs0cH_iZh0ZPOHE_gYmj1H3UCKZREw&usqp=CAU");
}
</style>