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
        <div class="container">
            <div class="row">
                <div class="col">
                    <h2>
                        Yu-Gi-Oh! API
                    </h2>
                </div>
            </div>

        </div>
    </header>
</template>

<style lang="scss" scoped>
header {
    padding: 40px;
    text-align: center;
}
</style>