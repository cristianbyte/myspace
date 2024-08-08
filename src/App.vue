<script setup lang="ts">
    import Banner from "./components/Banner.vue";
    import Profile from "./views/Profile.vue";
</script>

<template>
    <Banner/>
    <Profile/>

</template>

<style>
    .app{
        width: 100vw;
        height: 100vh;
        padding: 2% 10%;
        display: flex;
        align-items: center;
        justify-content: start;
        flex-direction: column;
        gap: 30px;
        background-color: var(--background);
    }
</style>
