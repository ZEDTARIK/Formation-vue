/* eslint-disable vue/require-v-for-key */
<template>
  <div class="container">
    <div class="row">
          <Courses />
    </div>
  </div>
</template>

<script>

import Courses from './components/Courses.vue';

export default {
  name: "App",
  components: {
    Courses
  },
  data() {
    return {
      
    };
  },
  methods: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
