<script>
import CardGame from './CardGame.vue';
import { store } from '../store.js';

export default {
    name: "MainComponent",
    data() {
        return {
            store
        }
    },
    methods: {

    },
    components: {
        CardGame
    },
    cardsNumber:{
        type:Number,
        default: 0,
    }
}
</script>

<template>
    <main>
        <div class="container">
            <div class="cardsNumber">
                <!-- Found {{ cardsNumber }} cards -->
            </div>
            <div class="row">
                <div class="col" v-for="(card, i) in store.cards" :key="i">
                    <CardGame :card="card" />
                </div>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
main{
    background-color: #d48f38;
    padding: 30px;
}

</style>