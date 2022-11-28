<template>
    <section class="bg-gray-100 mt-2">
        <div class="sticky top-12 z-20 bg-white py-1 font-bold">
            <Swiper :slides-per-view="3" :space-between="10" :slides-offset-after="10" :slides-offset-before="10"
                class="p-2 relative">
                <SwiperSlide class="rounded-lg bg-primary">
                    <p class=" text-white h-14 py-1 px-2 ">For You</p>
                </SwiperSlide>
                <SwiperSlide class="rounded-lg bg-purple-600">
                    <p class=" text-white h-14 py-1 px-2 ">Special Discount</p>
                </SwiperSlide>
                <SwiperSlide class="rounded-lg bg-yellow-600">
                    <p class=" text-white h-14 py-1 px-2 ">Galeri Fashion</p>
                </SwiperSlide>
                <SwiperSlide class="rounded-lg bg-red-500">
                    <p class=" text-white h-14 py-1 px-2 ">Dekorasi</p>
                </SwiperSlide>
            </Swiper>
        </div>
        <div class="flex flex-wrap">
            <div v-for="item in foryou_product" :key="item.id" class="w-1/2 p-2 ">
                <ProductCard :product="item" />
            </div>
        </div>
    </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import 'swiper/css'

const foryou_product = await useFetch('https://fakestoreapi.com/products?sort=desc').then(res => {
    return res.data
})
</script>

<style lang="scss" scoped>

</style>