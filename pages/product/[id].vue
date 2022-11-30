<template>
    <div>
        <div class="p-5">
            <img :src="data.image" :alt="data.title" class="w-screen aspect-square object-scale-down">
        </div>
        <div class="px-2 py-5 border-t-2 relative">
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
                    <p> {{ `${data.rating.rate}(${data.rating.count})` }} </p>
                </button>
            </div>
        </div>
        <div class="pb-5 px-2">
            <h1 class="font-semibold mb-2">Detail Produk</h1>
            <p class="mb-2 border-b">Kondisi : Baru</p>
            <p class="mb-2 border-b">Min Pembelian : 1pcs</p>
            <p class="mb-2 border-b">Kategori : {{ capitalize(data.category) }}</p>
            <h1 class="font-semibold mb-2">Deskripsi Produk</h1>
            {{ data.description }}
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