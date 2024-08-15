<script setup>
    import GraphIcon from "./icons/Chart.vue"
</script>
<template>
    <div class="timeline">
        <div class="timeline__head">
            <GraphIcon class="icon" />
            <h3>Activity Timeline</h3>
        </div>
    </div>

</template>
<style scoped>
    .timeline{
        display: flex;
        flex-direction: column;
        width: 70%;
        height: 100vh;
        background-color: transparent;
        border-radius: var(--border);
        border: 1px var(--shadow) solid ;
        padding: 1rem;
    }

    .timeline__head{
        display: flex;
        flex-direction: row;
        align-items: center;
        gap: .5rem;
        height: 2rem;
        line-height: 1rem;
        width: 100%;
        color: var(--text);
    }
</style>