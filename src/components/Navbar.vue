<script setup>
    import BurgerIcon from './icons/Burger.vue'
    import SearchIcon from './icons/Search.vue'
    import LanguageIcon from './icons/Language.vue'
    import Light from './icons/Light.vue'
    import Bell from './icons/Bell.vue'
    import imageProfile from '/profile.jpeg'
</script>

<template>
    <div class="navbar">
        <BurgerIcon class="iconButton"/>
        <SearchIcon class="iconButton"/>
        
        <div class="navbar__options">
            <LanguageIcon class="icon"/>
            <Light class="icon"/>
            <Bell class="icon"/>
            <div class="navbar__profile">
                <img :src="imageProfile" alt="Profile Picture"/>
            </div>
        </div>
    </div>
</template>


<style scoped>

    .icon:nth-of-type(1){
        fill: var(--accent);
    }

    .iconButton, .icon{
        transition: .2s ease;
        height: calc(100% - 10px);
        width: min-content;
        padding: 10px;
        margin: 6px 0;
        stroke: var(--accent);
    }
    
    .iconButton:hover, .icon:hover {
        cursor: pointer;
        border-radius: 50%;
        background-color: var(--hover);
    }

    .navbar {
        position: relative;
        display: flex;
        flex-direction: row;
        align-items: center;
        width: 100%;
        height: 6vh;
        padding: 0 2vw;
        background-color: var(--base);
        overflow: hidden;
        border-radius: var(--border);
        border: 1px var(--shadow) solid ;
    }

    .navbar__options{
        display: flex;
        height: inherit;
        align-items: center;
        margin-left: auto;
        width: 20%;
        width: max-content;
    }

    .navbar__options .navbar__profile{
        position: relative;
        height: 70%;
        aspect-ratio: 1/1;
        margin-left: 5px;
        cursor: pointer;
    }
    
    .navbar__profile img{
        border-radius: 50%;
    }

    .navbar__profile::after{
        position: absolute;
        content: '';
        width: 15px;
        height: 15px;
        border-radius: 50%;
        border: 3px solid var(--base);
        background-color: var(--aqua);
        bottom: 0;
        right: 0;
    }

</style>