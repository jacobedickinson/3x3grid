<template>
  <div>
    <table>
      <tr>
        <th>Firstname</th>
        <th>Lastname</th>
        <th>Age</th>
      </tr>
      <tr v-for="(person,index) in people">
        <td>{{person.firstName}}</td>
        <td>{{person.lastName}}</td>
        <td>{{person.personAge}}</td>
        <button @click="deleteTableRow">X</button>
      </tr>
    </table>
  </div>
</template>

<script>
export default {
  data() {
    return {
      people: [
        { firstName: "Jacob", lastName: "Dicksinson", personAge: 22 },
        { firstName: "Fred", lastName: "Jones", personAge: 24 },
      ],
    };
  },
  methods: {
    deleteTableRow: function (index) {
      this.people.splice(index, 1);
    },
  },
};
</script>

<style scoped>
table,
th,
td {
  border: 1px solid black;
}
</style>