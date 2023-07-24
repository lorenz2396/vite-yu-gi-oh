<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import MainComponent from "./components/MainComponent.vue";

import axios from "axios";
import { store } from './store.js';

export default {
  name: "App",
  components: {
      HeaderComponent,
      MainComponent,
  },
  data() {
    return {
      store
    };
  },
  methods: {
    getArchetype(){ 
      axios.get('https://db.ygoprodeck.com/api/v7/archetypes.php')
      .then(res=>{
      
        this.store.archetype=res.data
        
      }
      )
    },
  },
  created(){
      axios.get('https://db.ygoprodeck.com/api/v7/cardinfo.php?num=40&offset=0')
      .then(res=>{
        this.store.cards=res.data.data
      }
      )
  
  }
};
</script>

<template>
  <div class="background">
    
    <HeaderComponent/>

    <MainComponent/>
    
  </div>
</template>

<style lang="scss">
@use "assets/scss/main" as *;

.background{
  background-color: $orange-bg;
  min-height: 100vh;
}
</style>