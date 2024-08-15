<script setup>
    import About from "../components/About.vue"
    import Timeline from "../components/Timeline.vue"
</script>

<template>
    <div class="profile">
        <About />
        <Timeline/>
    </div>
</template>


<style scoped>

    .profile {
        width:  100%;
        height: 100%;
        max-width: 95vw;
        gap: 1rem;
        display: flex;
        align-items: start;
        height: max-content;
        scrollbar-width: none; /* Firefox */
    }

    @media (max-width: 800px) {
        .profile{
            flex-direction: column;

        }
        
    }
</style>