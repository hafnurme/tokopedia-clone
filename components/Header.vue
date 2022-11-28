<template>
    <header class="bg-primary px-3 py-5" ref="nav">
        <nav class="flex items-center">
            <input type="text" placeholder="Cari di Tokopedia"
                class="rounded-md border-2 outline-none placeholder:text-sm py-1 px-4 w-7/12">
            <div class="text-white flex justify-between flex-1 ml-3">
                <i class="material-icons">email</i>
                <i class="material-icons">notifications</i>
                <i class="material-icons">shopping_cart</i>
                <i class="material-icons">menu</i>
            </div>
        </nav>
        <div class="flex text-white text-sm items-center py-2" v-if="location_on">
            <span class="material-icons text-xs mr-1">location_on</span>
            <p>Dikirim ke <span class="font-bold">Matesih , Karanganyar</span></p>
            <span class="material-icons text-xs ml-1 pt-0.5">expand_more</span>
        </div>
    </header>
</template>

<script setup>
const nav = ref(null)
const location_on = ref(true)
onMounted(() => {
    document.body.addEventListener('wheel', () => {
        if (window.scrollY > 10) {
            nav.value.classList.add('nav-scrolled')
            location_on.value = false
        } else {
            nav.value.classList.remove('nav-scrolled')
            location_on.value = true
        }
    })
})

</script>

<style scoped>
.nav-scrolled {
    position: sticky;
    top: 0;
    left: 0;
    right: 0;
    background-color: white;
    z-index: 100;
    padding: 8px 10px;
}

.nav-scrolled input {
    border: 1px solid rgb(182, 182, 182);
}

.nav-scrolled i {
    color: #1c994e;
}
</style>