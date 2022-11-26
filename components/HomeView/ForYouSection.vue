<template>
    <section class="bg-gray-100">
        <div class="flex flex-wrap">
            <div v-for="item in foryou_product" :key="item.id" class="w-1/2 p-2 ">
                <ProductCard :product="item" />
            </div>
        </div>
    </section>
</template>

<script setup>
const foryou_product = await useFetch('https://fakestoreapi.com/products?sort=desc').then(res => {
    return res.data
})
</script>

<style lang="scss" scoped>

</style>