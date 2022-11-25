<template>

    <Swiper :slides-per-view="1" :autoplay="{
        delay: 4000,
        disableOnInteraction: true
    }" :modules="Modules">
        <SwiperSlide>
            <div class="rounded-lg overflow-hidden mx-2">
                <img src="../assets/image/banner/banner (1).jpg" alt="">
            </div>
        </SwiperSlide>
        <SwiperSlide>
            <div class="rounded-lg overflow-hidden mx-2">
                <img src="../assets/image/banner/banner (2).jpg" alt="">
            </div>
        </SwiperSlide>
    </Swiper>

</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'
import { Autoplay } from 'swiper'

const Modules = [Autoplay]
</script>