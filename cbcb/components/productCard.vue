<template>
    <div class="card text-center">
        <img :src="product.image" alt="product thumb" class="thumb">
        <p class="font-bold text-gray-500 m-4 truncate">{{ product.title }}</p>
        <nuxt-link :to="`/product/${product.id}`">
            <p class="btn my-4">View Details</p>
        </nuxt-link>
    </div>
</template>

<script>
export default {
    props: {
        product: {
            type: Object,
            required: true
        }
    }
}
</script>

<style lang="scss" scoped>
.thumb{
    max-height: 120px;
    max-width: 70%;
    margin: 0 auto;
}
</style>
