<template>
  <div class="shoppinglist">
    <h1 style="color: white">Shopping List</h1>
    <div>
      <div class="shoppingitem">
        <p>Cheese</p>
        <p>100 kr</p>

        <input class="mr-2 leading-tight" type="checkbox" :value="100" v-model="items" />
      </div>
      <br />
      <div class="shoppingitem">
        <p class="font-normal text-white">Coconut</p>
        <p>150 kr</p>
        <input type="checkbox" :value="150" v-model="items" />
      </div>
      <br />
      <div class="shoppingitem">
        <p>Cornflakes</p>
        <p>200 kr</p>
        <input type="checkbox" :value="200" v-model="items" />
      </div>
    </div>
    <span v-text="totalCost"></span>
    kr.
  </div>
</template>

<script>
export default {
  data() {
    return {
      price: 0,
      items: [],
    };
  },
  computed: {
    totalCost: function () {
      return this.items.reduce((sum, item) => sum + item, this.price);
    },
  },
};
</script>

<style scoped>
.shoppinglist {
  background-color: cornflowerblue;
}
.shoppingitem {
  background-color: cornsilk;
  display: inline-flex;
  margin: 2em;
  padding: 2em;
  border-radius: 5px;
}
input {
  margin-top: 1.5em;
}
</style>