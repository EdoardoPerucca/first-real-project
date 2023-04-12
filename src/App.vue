<script>

import { store } from "./store.js";

import '@fortawesome/fontawesome-free/css/all.css';

import HeaderApp from "./components/HeaderApp.vue";
import MainApp from "./components/MainApp.vue";
import FooterApp from "./components/FooterApp.vue";

export default {

  data() {

    return {
      store,
    }
  },

  components: {
    HeaderApp,
    MainApp,
    FooterApp
  },


}
</script>

<template>
  <HeaderApp></HeaderApp>

  <MainApp></MainApp>

  <FooterApp></FooterApp>
</template>

<style scoped lang="scss"></style>
