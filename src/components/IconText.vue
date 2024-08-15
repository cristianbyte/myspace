<script setup lang="ts">
    import { defineProps } from 'vue';

    const props = defineProps<{
    styleType?: string // Definido como opcional
    }>();
</script>

<template>
    <div :class="['icon__text', styleType ? styleType : '']">
        <slot></slot>
    </div>
</template>

<style >
    .icon__text{
        transition: .3s ease-out;
        display: flex;
        justify-content: start;
        align-items: center;
        gap: 5px;
        width: max-content;
        font-size: .9rem;
        color: var(--accent);
        fill: var(--accent);
    }
    
    .tabs {
        color: var(--accent);
        fill: var(--accent);
    }

    .tabs:hover{
        color: var(--slate);
        fill: var(--slate);
    }

</style>