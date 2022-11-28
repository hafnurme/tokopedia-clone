<template>
    <section>
        <div>
            <div class="px-5 pb-5">
                <h3 class="font-semibold">Jangan Lewatkan Promonya!</h3>
                <div class="text-xs flex justify-between mt-1">
                    <div>
                        <span>Berakhir dalam</span>
                        <span class="mx-1 bg-red-600 px-4 py-0.2 rounded-full text-white">8:46:5</span>
                    </div>
                    <a class="text-green-600 font-bold">Lihat Semua</a>
                </div>
            </div>
            <div>
                <div class="bg-primary relative h-64 py-[10px] box-border">
                    <img src="~/assets/image/banner/diskon.png" alt="" class="h-full absolute top-0 left-0 mx-2">
                    <Swiper :slides-per-view="3" :space-between="10" :slides-offset-before="111"
                        :slides-offset-after="20">
                        <SwiperSlide v-for="product in products" :key="product.id" class="h-36">
                            <ProductCard :product="product" />
                        </SwiperSlide>
                    </Swiper>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'
import axios from 'axios'

const products = await useFetch('https://fakestoreapi.com/products?limit=10').then((res) => {
    return res.data
})
</script>

<style lang="scss" scoped>

</style>