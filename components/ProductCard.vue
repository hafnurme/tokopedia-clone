<template>
    <div class="flex flex-col bg-white rounded-md overflow-hidden w-full h-[236px]">
        <div class="flex items-center justify-center h-32">
            <img :src="product.image" alt="" class="max-h-[6rem]">
        </div>
        <div class="p-2 flex-1 flex flex-col border-t-4 gap-1">
            <p class="font-bold">
                {{ new Intl.NumberFormat('en-US', { style: 'currency', currency: 'USD' }).format(product.price) }}
            </p>
            <div class="text-xs bg-red-200 text-red-800 w-fit rounded-md px-1 font-semibold">- 10%</div>
            <p class="truncate text-sm">{{ product.title }}</p>
        </div>

    </div>
</template>

<script setup>
defineProps(['product'])
</script>

<style lang="scss" scoped>

</style>