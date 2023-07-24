<script>
import { store } from '../store.js';

export default {
    name: "HeaderComponent",
    data() {
        return {
            store
        }
    },
    methods: {

    }
}
</script>

<template>
    <header class="text-start">
        <div class="p-2">
            <div class="row">
                <div class="col d-inline-flex">
                    <div class="img-container">
                        <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/11/Yu-Gi-Oh%21_%28Logo%29.jpg/800px-Yu-Gi-Oh%21_%28Logo%29.jpg" alt="">
                    </div>
                    <div class="col">
                        <h2>
                            Yu-Gi-Oh! API
                        </h2>
                    </div>
                </div>
            </div>    
        </div>
    </header>
</template>

<style lang="scss" scoped>
header{

background-color: white;
border-bottom: solid 1px black;
.img-container{
    height: 2rem;

    img{
        height: 100%;
    }
}
}
</style>