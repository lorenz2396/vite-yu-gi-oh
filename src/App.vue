<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import MainComponent from "./components/MainComponent.vue";
import FooterComponent from "./components/FooterComponent.vue";

import axios from "axios";
import { store } from './store.js';

export default {
  name: "App",
  components: {
      HeaderComponent,
      MainComponent,
      FooterComponent,
  },
  data() {
    return {
      store
    };
  },
  methods: {},
  created() {
        axios
            .get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0')
            .then(response => {
                console.log(response);
                this.store.cards = response.data.data;
            });
    }
};
</script>

<template>

  <HeaderComponent/>

  <MainComponent/>

  <FooterComponent/>

</template>

<style lang="scss">
@use "assets/scss/main";
</style>