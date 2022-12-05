<template>
    <main>
        <div class="m-5">
            <h1 class="font-bold text-lg mb-2">Nonton yang seru seru</h1>
            <div class="flex gap-2">
                <div v-for="i in 4" :key="i">
                    <FeedViewLiveCardComponent :index="i" />
                </div>
            </div>
        </div>

        <div v-for="i in 5" :key="i">
            <FeedCardComponent />
        </div>

    </main>
</template>
