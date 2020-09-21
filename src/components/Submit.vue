<template>
  <div>
    <div>
      <table>
        <tr>
          <th>Firstname</th>
          <th>Lastname</th>
          <th>Age</th>
        </tr>
        <tr v-for="person in people">
          <td>{{person.firstName}}</td>
          <td>{{person.lastName}}</td>
          <td>{{person.personAge}}</td>
        </tr>
        <td>
          <input type="text" placeholder="First" v-model="newPerson.firstName" />
        </td>
        <td>
          <input type="text" placeholder="last" v-model="newPerson.lastName" />
        </td>
        <td>
          <input type="text" placeholder="age" v-model="newPerson.personAge" />
        </td>
      </table>
      <button @click="addNewPerson(people)">Submit</button>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      people: [
        { firstName: "Jacob", lastName: "Dicksinson", personAge: "22" },
        { firstName: "Fred", lastName: "Jones", personAge: "24" },
      ],
      newPerson: {
        firstName: "",
        lastName: "",
        personAge: "",
      },
    };
  },
  methods: {
    addNewPerson() {
      this.people.push(this.newPerson);
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