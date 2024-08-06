<script setup lang="ts">
    import CalendarIcon from './icons/Calendar.vue'
    import LocationIcon from './icons/Location.vue'
    import PaletteIcon from './icons/Palette.vue'
    import imageProfile from '/profile.jpeg'

</script>

<template>
    <div class="banner">
        <div class="profile">
            <div class="profile__image">
                <img :src="imageProfile" alt="Profile Image">
            </div>
            <div class="profile__data">
                <h3> Jhonson Dae</h3>

            </div>
        </div>
    </div>
</template>

<style scoped>
   .banner {
        position: relative;
        display: flex;
        align-items: end;
        width: 80vw;
        max-width: 1000px;
        background-image: linear-gradient(50deg, var(--main) 30%, var(--accent)70%);
        height: 30vh;
        border-radius: 1vw;
        overflow: hidden;
        box-shadow: 0 0 .5rem var(--gray);
   }

   .profile{
        height: 40%;
        width: 100%;
        padding: 0 2%;
        background-color: var(--white);
   }

   .profile__image{
        height: calc(100% + 2rem);
        aspect-ratio: 1/1;
        object-fit: fill;
        transform: translateY(-40%);
        z-index: 100;
    }
    .profile__image img{
        width: 100%;
        height: 100%;
        border: .4rem solid var(--white);
        border-radius: 50%;
    }

</style>
