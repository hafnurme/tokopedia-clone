<template>
    <div class=" overflow-hidden rounded-lg relative">
        <div class="absolute top-2 left-1.5 text-xs text-white rounded overflow-hidden">
            <span class="p-0.5 pl-1 bg-red-500">Live</span>
            <span class="p-0.5 pr-1 bg-gray-700">100</span>
        </div>
        <img :src="`https://picsum.photos/100/150?random=${index}`" alt="">
        <p class="absolute bottom-0 text-[14px] p-2 text-white font-bold ">Lorem ipsum dolor</p>
    </div>
</template>

<script setup>
const props = defineProps(['index'])
console.log(props)
</script>