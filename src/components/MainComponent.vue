<script>
import {store} from '../store.js'
import CardGame from './CardGame.vue'

export default {
    name: "MainComponent",
    components:{
        CardGame,
    },
    data() {
        return {
            store,
        }
    },
    methods: {
     
    },
}
</script>

<template>
    <main>

        <div class="container">

            <div class="row">

                <div class="col-auto px-2 my-3">


                </div>

            </div>


            <div class="row flex-wrap row-cols-5 card-container justify-content-between align-items-start mx-3 g-2">

                <div v-for="(card,i) in store.cards" :key="i"  class="col p-3">
                    
                    <CardGame :cardData="card"/> 

                </div>

            </div>

        </div>

        
    </main>
</template>

<style lang="scss" scoped>

.card-container{
    background-color: white;
}

</style>