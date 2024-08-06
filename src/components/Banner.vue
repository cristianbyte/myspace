<script setup lang="ts">
    import CalendarIcon from './icons/Calendar.vue'
    import LocationIcon from './icons/Location.vue'
    import PaletteIcon from './icons/Palette.vue'
    import ConnectIcon from './icons/Connect.vue'
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
                <div class="profile__links">
                    <span href="#" class="profile__link">
                        <PaletteIcon class="icon" />
                        <p>Colors</p>
                    </span>
                    <span href="#" class="profile__link">
                        <CalendarIcon class="icon" />
                        <p>Events</p>
                    </span>
                    <span href="#" class="profile__link">
                        <LocationIcon class="icon" />
                        <p>Location</p>
                    </span>
                </div>
            </div>
            <div class="profile__actions">
                <button class="profile__status">
                    <ConnectIcon class="icon"/>
                    <p>Connected</p>
                </button>
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
        max-width: 1200px;
        background-image: conic-gradient(from -140deg at 60% 70%, var(--helper) 0% 35%, var(--accent) 45% 50%, var(--helper) 60% 95%) ;
        height: 30vh;
        border-radius: 5px;
        overflow: hidden;
        box-shadow: 0 0 .5rem var(--gray);
   }

   .profile{
        height: 40%;
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: start;
        gap: 2%;
        padding: 0 2%;
        background-color: var(--white);
   }

   .profile__image{
        height: 100%;
        aspect-ratio: 1/1;
        object-fit: fill;
        transform: translateY(-40%);
        z-index: 100;
    }

    .profile__image img{
        width: 100%;
        height: 100%;
        border: .4rem solid var(--white);
        border-radius: 5%;
    }

    .profile__data{
        display: flex;
        justify-content: center;
        flex-direction: column;
        align-items: start;
        gap: 10%;
        width: 100%;
    }

    .profile__links{
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        gap: 1rem;
        justify-content: space-between;
        height: 20%;
    }

    .profile__link{
        transition: .3s ease;
        cursor: pointer;
        display: flex;
        height: 10px;
        flex-direction: row;
        align-items: center;
        gap: 5px;
    }

    
    .profile__link svg{
        height: 20px;
    }
    
    .profile__link{
        fill: var(--gray);
        color: var(--gray);
    } 
    .profile__link:hover {
        color: var(--invert);
        fill: var(--invert);
    }

    .profile__actions{
        position: absolute;
        bottom: 10%;
        right: 2vw;
    }

    .profile__actions .profile__status{
        transition: .3s ease;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 5px;
        height: 30px;
        background-color: var(--main);
        color: var(--white);
        border: none;
        cursor: pointer;
        padding: 10%;
        font-size: .8rem;
        border-radius: .5rem;
    }

    .profile__status svg{
        fill: var(--white);
        height: 20px;
        width: 40px;
    }

</style>
