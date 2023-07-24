<script>
export default {
    data() {
        return {
        }
    },
    props:{
        cardData:{
            type:Object,
            defult: null
        }
    }  
}
</script>

<template>

    <div class="col p-3">

        <div class="card">

            <div class="img-container card-img-top">
                
                <img :src="cardData.card_images[0].image_url" :alt="cardData.name">

            </div>

            <div class="card-body">

                <h5 class="card-title">{{ cardData.name }}</h5>

                <p class="card-text">{{ cardData.archetype }}</p>

            </div>

        </div>

    </div>
</template>

<style lang="scss" scoped>
@use '../assets/scss/partials/variables'as*;
    .img-container{
    width: 100%;

    img{
        width: 100%;
    }
    
    }

    .card-body{
        background-color: $orange-bg;
    }

  

</style>