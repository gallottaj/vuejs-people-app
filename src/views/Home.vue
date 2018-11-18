<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <ul>
        <li v-for="person in people">name: {{ person.name }} bio: {{ person.bio }} bioVisible: {{ person.bioVisible }}</li>
    </ul>
    <p>name:<input type="text" v-model="newPerson.name"></p>
    <p>bio:<input type="text" v-model="newPerson.bio"></p>
    <p>bioVisible:<input type="text" v-model="newPerson.bioVisible"></p>
    <p><button v-on:click="addPerson()">Click to add a person</button></p>
  </div>
</template>

<style>
</style>

<script>
export default {
  data: function() {
    return {
      message: "Welcome to Vue.js!",
      people: [
        {name: "tom" , bio: "all about tom", bioVisible: "true"},
        {name: "dan" , bio: "all about dan", bioVisible: "true"}
      ],
      newPerson: {name: "" , bio: "", bioVisible: "true"}
    };
  },
  created: function() {},
  methods: {
    addPerson: function() {
      console.log('adding the person...');
      var newPerson = {name: "" , bio: "", bioVisible: "true"};
      this.people.push(newPerson);
    }
  },
  computed: {}
};
</script>



