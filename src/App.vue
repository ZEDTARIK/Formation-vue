/* eslint-disable vue/require-v-for-key */
<template>
  <div class="container">
    <Courses />
    <Footer>
      <div class="text-center p-3"> © 2020 Copyright:
            <a class="" href="http://localhost:8080/">Zouhair ETTARAK</a>
        </div>
    </Footer>
  </div>
</template>

<script>

import Courses from './components/Courses.vue';
import Footer from './components/shared/Footer';

export default {
  name: "App",
  components: {
    Courses,
    Footer
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
