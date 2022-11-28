<template>
    <div class="px-5">
        <h1 class="mb-2">Cari semua di Tokopedia!</h1>
        <div>
            <div class="flex justify-between border-b py-2 cursor-pointer" @click="handleExpand">
                <h3>Promo</h3>
                <i class="material-icons">expand_more</i>
            </div>
            <ul class="text-sm text-slate-800 hidden" ref="ul">
                <li>
                    <p>Waktu Indonesia Belanja</p>
                </li>
                <li>
                    <p>Bebas Ongkir</p>
                </li>
                <li>
                    <p>Waktu Indonesia Belanja TV Show</p>
                </li>
                <li>
                    <p>Kejar Diskon</p>
                </li>
                <li>
                    <p>Flash Sale</p>
                </li>
                <li>
                    <p>Promo Pengguna Baru</p>
                </li>
                <li>
                    <p>Tokopedia Nyam</p>
                </li>
                <li>
                    <p>Bangga Buatan Indonesia</p>
                </li>
                <li>
                    <p>Tap Tap Kotak</p>
                </li>
                <li>
                    <p>Tokopedia Peduli Sehat</p>
                </li>
                <li>
                    <p>Home Living Salebration</p>
                </li>
                <li>
                    <p>Serbu Official Store</p>
                </li>
                <li>
                    <p>Tokopedia Parents</p>
                </li>
                <li>
                    <p>Cantik Fest</p>
                </li>
                <li>
                    <p>GOPAY COINS</p>
                </li>
                <li>
                    <p>Kebut Tokopedia Gopay</p>
                </li>
                <li>
                    <p>Hari Libur Nasional</p>
                </li>
            </ul>
        </div>
        <div class="py-4 border-b">
            <h3 class="mb-2">Mau cari apa di Tokopedia ?</h3>
            <div class="text-xs text-slate-800">Promo | Kategori | Official Store | Tokopedia Salam | Tiket Pesawat |
                Tiket
                Kereta Api |
                Hotel | Deals |
                Blog | Situs Desktop</div>
        </div>
    </div>
</template>

<script setup>
const ul = ref(null)
const handleExpand = () => {
    ul.value.classList.toggle('hidden')
}

</script>

<style scoped>
ul li {
    margin: 10px 0;
}
</style>