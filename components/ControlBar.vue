<template>
    <div class="py-5 overflow-visible">
        <Swiper :slides-per-view="5" :space-between="0" :slides-per-group="5" :slides-offset-before="10"
            :slides-offset-after="10">
            <SwiperSlide>
                <div class="control-icon">
                    <img src="@/assets/image/promo.png" alt="" class="w-9">
                    <p class="text-xs h-10 w-full flex items-center justify-center">Promo</p>
                </div>
            </SwiperSlide>
            <SwiperSlide>
                <div class="control-icon">
                    <img src="@/assets/image/lihat_semua.png" alt="" class="w-9">
                    <p class="text-xs h-10 w-full flex items-center justify-center">Lihat Semua</p>
                </div>
            </SwiperSlide>
            <SwiperSlide>
                <div class="control-icon">
                    <img src="@/assets/image/toserba.png" alt="" class="w-9">
                    <p class="text-xs h-10 w-full flex items-center justify-center">Toserba</p>
                </div>
            </SwiperSlide>
            <SwiperSlide>
                <div class="control-icon">
                    <img src="@/assets/image/gaming.png" alt="" class="w-9">
                    <p class="text-xs h-10 w-full flex items-center justify-center">Gaming</p>
                </div>
            </SwiperSlide>
            <SwiperSlide>
                <div class="control-icon">
                    <img src="@/assets/image/topup.png" alt="" class="w-9">
                    <p class="text-xs h-10 w-full flex items-center justify-center">Top-Up & Tagihan</p>
                </div>
            </SwiperSlide>
            <SwiperSlide>
                <div class="control-icon">
                    <img src="@/assets/image/stationery.png" alt="" class="w-9">
                    <p class="text-xs h-10 w-full flex items-center justify-center">Office & Stationery</p>
                </div>
            </SwiperSlide>>
        </Swiper>
    </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
const controlbar = [
    {
        name: 'promo',
        label: 'Promo Hari Ini'
    },
    {
        name: 'lihat_semua',
        label: 'Lihat Semua'
    },
    {
        name: 'toserba',
        label: 'Toserba'
    },
    {
        name: 'kesehatan',
        label: 'Kesehatan'
    },
    {
        name: 'topup',
        label: 'Top-Up & Tagihan'
    },
    {
        name: 'travel',
        label: 'Travel & Entertaiment'
    },
    {
        name: 'keuangan',
        label: 'Keuangan'
    },
    {
        name: 'stationery',
        label: 'Office & Stationery'
    },
    {
        name: 'makanan',
        label: 'Makanan & Minuman'
    },
    {
        name: 'perawatan',
        label: 'Perawatan Hewan'
    },
    {
        name: 'gaming',
        label: 'Gaming'
    },
    {
        name: 'komputer',
        label: 'Komputer & Laptop'
    },
]

</script>

<style scoped>

</style>