<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <ol>
        <li v-for="people in peoples">name: {{ people.name }} bio: {{ people.bio }} bioVisible: {{ people.bioVisible }}</li>
    </ol>
  </div>
</template>

<style>
</style>

<script>
export default {
  data: function() {
    return {
      message: "Welcome to Vue.js!",
      peoples: [
        {name: "tom" , bio: "all about tom", bioVisible: "true"},
        {name: "dan" , bio: "all about dan", bioVisible: "true"}
      ]
    };
  },
  created: function() {},
  methods: {},
  computed: {}
};
</script>



