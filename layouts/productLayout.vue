<template>
    <div class="max-w-[460px] relative mx-auto">
        <header class="sticky top-0 bg-white">
            <nav class="flex items-center p-2">
                <router-link to="/" class="material-icons text-primary mr-2 ">arrow_back_ios</router-link>
                <input type="text" placeholder="Cari di Tokopedia"
                    class="rounded-md border-2 outline-none placeholder:text-sm py-1 px-4 w-7/12">
                <div class="text-primary flex justify-between flex-1 ml-5">
                    <i class="material-icons">share</i>
                    <i class="material-icons">shopping_cart</i>
                    <i class=" material-icons">menu</i>
                </div>
            </nav>
        </header>
        <slot />
        <footer class="flex p-2 items-center gap-2 sticky bottom-0 bg-white">
            <span class="material-icons rounded-md border p-1 border-primary ">
                chat
            </span>
            <button class="flex-1 rounded-md py-1 border border-primary text-primary">Beli</button>
            <button class="flex-1 rounded-md py-1 border border-primary text-white bg-primary ">+ Keranjang</button>
        </footer>
    </div>
</template>