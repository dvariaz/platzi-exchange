<template>
    <div id="app">
        <main>
            <px-header :links="links" />
            <router-view
                class="container px-5 sm:px-20 py-20 flex-column justify-center"
            />
        </main>
    </div>
</template>

<script>
import PxHeader from "@/components/PxHeader.vue";

export default {
    name: "App",
    components: { PxHeader },
    data() {
        return {
            links: [
                {
                    title: "BTC",
                    to: { name: "coin-detail", params: { id: "bitcoin" } }
                },
                {
                    title: "ETH",
                    to: { name: "coin-detail", params: { id: "ethereum" } }
                },
                {
                    title: "XRP",
                    to: { name: "coin-detail", params: { id: "xrp" } }
                }
            ]
        };
    }
};
</script>

<style>
#app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}
</style>
