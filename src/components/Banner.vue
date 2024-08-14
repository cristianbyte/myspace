<script setup lang="ts">
    import CalendarIcon from './icons/Calendar.vue'
    import LocationIcon from './icons/Location.vue'
    import PaletteIcon from './icons/Palette.vue'
    import ConnectIcon from './icons/Connect.vue'
    import imageProfile from '/profile.jpeg'
    import IconText from './IconText.vue'

</script>

<template>
    <div class="banner">
        <div class="banner__back"></div>
        <div class="profile">
            <div class="profile__image">
                <img :src="imageProfile" alt="Profile Image">
            </div>
            <div class="profile__data">
                <h3> Jhonson Dae</h3>
                <div class="profile__links">
                    <IconText>
                        <PaletteIcon class="icon" />
                        <p>UX Designer</p>
                    </IconText>
                    <IconText>
                        <LocationIcon class="icon" />
                        <p>Medellin, CO</p>
                    </IconText>
                    <IconText>
                        <CalendarIcon class="icon" />
                        <p>Joined August 2021</p>
                    </IconText>
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
        flex-direction: column;
        width: 100%;
        height: 30vh;
        max-height: 35vh;
        border-radius: var(--border);
        border: 1px var(--shadow) solid ;
        overflow: hidden;
   }

   .banner__back{
        width: 100%;
        height: 100%;
        background-image: url(/background.png);
        background-size: 100% 100%;
   }

   .profile{
       height: 40%;
       width: 100%;
       display: flex;
       flex-direction: row;
       justify-content: start;
       gap: 2%;
       padding: 0 2%;
       background-color: var(--base);
   }

   .profile__image{
        width: 8rem;
        height: 8rem;
        aspect-ratio: 1/1;
        object-fit: fill;
        transform: translateY(-20%);
        z-index: 100;
    }

    .profile__image img{
        width: 100%;
        height: 100%;
        border: .4rem solid var(--base);
        border-radius: var(--border);
        overflow: hidden;
    }

    .profile__data{
        display: flex;
        justify-content: center;
        flex-direction: column;
        align-items: start;
        width: 100%;
        gap: 1rem;
        color: var(--text);
    }

    .profile__links{
        display: flex;
        width: 100%;
        height: min-content;
        flex-direction: row;
        justify-content: start;
        align-items: center;
        flex-wrap: wrap;
        color: var(--accent);
        gap: 1rem;
    }
    
    .profile__link{
        transition: .3s ease;
        cursor: pointer;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        gap: 10px;
    }
    
    
    .profile__actions{
        position: absolute;
        bottom: 20%;
        right: 5vw;
    }

    .profile__actions .profile__status{
        transition: .3s ease;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 0px;
        height: 40px;
        width: max-content;
        background-color: var(--slate);
        color: var(--base);
        border: none;
        cursor: pointer;
        padding: 5% 10% 5% 5%;
        font-size: .8rem;
        border-radius: .5rem;
    }

    .profile__status svg{
        fill: var(--base);
        height: 20px;
        width: 30px;
    }

    @media (max-width: 600px) {
        .banner{
            height: 40vh;
        }
        .profile{
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 70%;
            gap: 0;
        }

        .profile__image, .profile__data{
            justify-content: start;
            align-items: center;
            transform: translateY(-50%);
        }

        .profile__links{
            justify-content: center;
        }

        .profile__actions{
            position: relative;
            height: 10vh;
            right: 0;
            bottom: 10%;
        }
    }

</style>
