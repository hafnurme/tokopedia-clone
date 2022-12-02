<template>
    <div>
        <div class="p-5">
            <img :src="data.image" :alt="data.title" class="w-screen aspect-square object-scale-down">
        </div>
        <div class="p-5 border-t-2 relative">
            <span class="material-icons absolute top-5 right-5">
                favorite
            </span>
            <h3 class="text-3xl font-bold mb-3">{{ new Intl.NumberFormat('en-US', {
                    style: 'currency', currency: 'USD'
                }).format(data.price)
            }}</h3>
            <p class="mb-3">{{ data.title }}</p>
            <div class="flex">
                <p>Terjual {{ data.rating.count }}+</p>
                <button class="ml-2 flex items-center text-sm border rounded px-3 pr-5"><span
                        class="material-icons text-yellow-300 text-sm mr-1">
                        star
                    </span>
                    <p> {{ `${data.rating.rate} (${data.rating.count})` }} </p>
                </button>
            </div>
        </div>
        <div class="px-5">
            <div class="mb-5">
                <h1 class="mb-2 font-bold text-lg">Detail Produk</h1>
                <p class="mb-2 border-b pb-1">Kondisi : Baru</p>
                <p class="mb-2 border-b pb-1">Min Pembelian : 1pcs</p>
                <p class="mb-2 border-b pb-1">Kategori : <span class="text-primary">{{
                        capitalize(data.category)
                }}</span></p>
            </div>
            <div class="my-5 border-b pb-5">
                <h1 class="font-bold text-lg mb-2">Deskripsi Produk</h1>
                <p>{{ data.description }}</p>
            </div>
        </div>
        <div class="flex px-3 items-center">
            <div class="bg-slate-300 w-12 h-12 rounded-full mr-3">
                <img src="~/assets/image/tokopedia.png" alt="logo toko" class="h-12 aspect-square object-scale-down">
            </div>
            <div>
                <h1 class="font-bold text-lg">Tokopedia Store</h1>
                <p class="text-xs mb-1">Jakarta</p>
                <p class="text-xs">Online <span>23 menit yang lalu</span></p>
            </div>
        </div>
        <div class="px-5    ">
            <div class="flex items-center">
                <span class="material-icons mr-1 text-sm ">
                    star_rate
                </span><span>4.5 rata-rata ulasan</span>
            </div>
            <div class="flex items-center mb-5">
                <span class="material-icons mr-1 text-sm ">
                    schedule
                </span><span> + 3 jam pesanan diproses</span>
            </div>
            <div class="my-2 py-5 border-y">
                <h1 class="text-lg font-bold mb-2">Ongkir Reguler $1 - $2 </h1>
                <p>Dikirim ke Matesih , Karanganyar</p>
                <p>Estimasi 2 - 3 Hari</p>
            </div>
            <div class="my-5">
                <h3 class="my-3 text-lg font-bold">Ulasan Pembeli</h3>
                <div class="flex items-center mb-2">
                    <div><img src="~/assets/image/user.jpg" alt="useravatar" class="rounded-full w-9 mr-2"></div>
                    <div>
                        <span class="font-bold">Putri Liam</span>
                    </div>
                </div>
                <p class="mb-1"> <span class="material-icons mr-1 text-sm text-yellow-400">
                        star_rate star_rate star_rate star_rate star_rate
                    </span>1 hari yang lalu</p>
                <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Adipisci sed, magni ad maiores possimus,
                    mollitia, minus quae voluptatibus in inventore quos! Vero vel ducimus minus officiis autem tempora
                    perferendis maxime.</p>
            </div>
        </div>
    </div>
</template>

<script setup>
import axios from 'axios';
import { capitalize } from 'vue';

const route = useRoute()
const data = await axios.get(`https://fakestoreapi.com/products/${route.params.id}`).then(res => {
    return res.data
})
definePageMeta({
    layout: 'product-layout'
})



</script>