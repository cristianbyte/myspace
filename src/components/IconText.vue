<template>
    <div class="icon__text">
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
        font-size: .8rem;
        color: var(--gray);
        fill: var(--gray);
        cursor: pointer;
    }
    

    .icon__text:hover{
        color: var(--invert);
        fill: var(--invert);
    }
</style>