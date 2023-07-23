<script>
export default {
    props: {
        card: {
            type: Object,
            default: {
                card_images: '',
                name: '',
                archetype: '',
                img_url:'',
            }
        }
    }
    
}
</script>

<template>
    <div class="single-card text-center m-4">
        <div>
            <img :src="card.card_images[0].img_url" :alt="card.name">
        </div>
        <div class="mb-4">
            <h3>
                {{ card.name }}
            </h3>
        </div>
        <div>
            <p class="mb-0">
                {{ card.archetype }}
            </p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
</style>