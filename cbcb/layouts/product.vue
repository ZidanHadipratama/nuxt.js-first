<template>
    <div>
        <header class="shadow-sm bg-white">
            <nav class="container mx-auto p-4 flex justify-between">
                <nuxt-link to="/">Product</nuxt-link>
                <ul class="flex gap-4">
                    <li><nuxt-link to="/">Home</nuxt-link></li>
                    <li><nuxt-link to="/about">About</nuxt-link></li>
                    <li><nuxt-link to="/product" class="btn">Product</nuxt-link></li>
                </ul>
            </nav>
        </header>

        <div class="container mx-auto p-4">
            <slot/>
        </div>

        <footer class="container mx-auto p-4 flex justify-between border-t-2">
            <ul class="flex gap-4">
                <li><nuxt-link to="/">Home</nuxt-link></li>
                <li><nuxt-link to="/about">About</nuxt-link></li>
                <li><nuxt-link to="/product">Product</nuxt-link></li>
            </ul>
        </footer>
    </div>
</template>

<script>
    export default {
    }
</script>

<style lang="scss" scoped>

</style>