<template>
    <div>
        <div class="grid grid-cols-4 gap-5">
            <div v-for="p in products">
                <productCard :product="p"/>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        async created () {
            definePageMeta({
                layout: 'product'
            });

            this.products = await useFetch('https://fakestoreapi.com/products').data

            useHead({
                title: 'Testing | Product',
                meta: [
                    {name: 'description', content: 'Nuxt 3 Merch'}
                ]
            })
        },
        data() {
            return {
                products: null
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>