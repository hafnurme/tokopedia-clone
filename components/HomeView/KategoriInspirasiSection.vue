<template>
    <div>
        <h3 class="p-5 font-semibold">Kategori inspirasi belanjamu</h3>
        <Swiper :slides-per-view="3" :space-between="10" :slides-offset-after="10" :slides-offset-before="10"
            :modules="Modules">
            <SwiperSlide>
                <div class="border rounded-md overflow-hidden text-center mb-4">
                    <img src="~/assets/image/category/dapur.jpg" alt="">
                    <p class="p-2 text-xs truncate">Dapur</p>
                </div>
                <div class="border rounded-md overflow-hidden text-center mb-4">
                    <img src="~/assets/image/category/fashion_pria.jpg" alt="">
                    <p class="p-2 text-xs truncate">Fashion Pria</p>
                </div>
            </SwiperSlide>
            <SwiperSlide>
                <div class="border rounded-md overflow-hidden text-center mb-4">
                    <img src="~/assets/image/category/handphone_tablet.jpg" alt="">
                    <p class="p-2 text-xs truncate">Handphone & Tablet</p>
                </div>
                <div class="border rounded-md overflow-hidden text-center mb-4">
                    <img src="~/assets/image/category/fashion_wanita.jpg" alt="">
                    <p class="p-2 text-xs truncate">Fashion Wanita</p>
                </div>
            </SwiperSlide>
            <SwiperSlide>
                <div class="border rounded-md overflow-hidden text-center mb-4">
                    <img src="~/assets/image/category/film_musik.jpg" alt="">
                    <p class="p-2 text-xs truncate">Film & Musik</p>
                </div>
                <div class="border rounded-md overflow-hidden text-center mb-4">
                    <img src="~/assets/image/category/kamera.jpg" alt="">
                    <p class="p-2 text-xs truncate">Kamera</p>
                </div>
            </SwiperSlide>
            <SwiperSlide>
                <div class="border rounded-md overflow-hidden text-center mb-4">
                    <img src="~/assets/image/category/kosmetik.jpg" alt="">
                    <p class="p-2 text-xs truncate">Kosmtik</p>
                </div>
                <div class="border rounded-md overflow-hidden text-center mb-4">
                    <img src="~/assets/image/category/mainan.jpg" alt="">
                    <p class="p-2 text-xs truncate">Hoby & Mainan</p>
                </div>
            </SwiperSlide>
            <SwiperSlide>
                <div class="border rounded-md overflow-hidden text-center mb-4">
                    <img src="~/assets/image/category/olahraga.jpg" alt="">
                    <p class="p-2 text-xs truncate">Olahraga</p>
                </div>
                <div class="border rounded-md overflow-hidden text-center mb-4">
                    <img src="~/assets/image/category/otomotif.jpg" alt="">
                    <p class="p-2 text-xs truncate">Otomotif</p>
                </div>
            </SwiperSlide>
        </Swiper>
    </div>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import 'swiper/css'
import 'swiper/css/grid'
import { Grid } from "swiper";

const Modules = [Grid]
</script>

