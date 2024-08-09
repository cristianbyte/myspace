<script setup lang="ts">
    import { ref, computed } from 'vue';
    import Banner from "./components/Banner.vue";
    import Profile from "./views/Profile.vue";
    import Teams from "./views/Teams.vue";
    import IconText from "./components/IconText.vue";
    import Account from "./components/icons/Account.vue";
    import Team from "./components/icons/Team.vue";

    const tabs = ref([
        { name: "Profile", icon: Account, styleType: 'tabs' },
        { name: "Teams", icon: Team, styleType: 'tabs' }
    ]);
    const activeComponent = ref('Profile');

    const componentMap = {
        Profile,
        Teams
    };

    const currentComponent = computed(() => componentMap[activeComponent.value]);

</script>

<template>

  <Banner/>

    <div class="buttons">
        <button 
        v-for='tab in tabs' 
        :key='tab.name' 
        @click='activeComponent = tab.name'
        :class="{'buttons__item': true, 'buttons__item--active': tab.name === activeComponent}" 
        >
            <IconText :class="tab.styleType">
                <component :is="tab.icon" class="icon"/>
                {{ tab.name }}
            </IconText>
        </button>
    </div>

  <component :is="currentComponent"/>

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
        gap: 10px;
        background-color: var(--background);
    }

    .buttons{
        display: flex;
        justify-content: start;
        align-items: center;
        gap: 20px;
        width: 100%;
    }

    .buttons__item{
        transition: all 0.4s ease;
        background-color: var(--background);
        color: var(--shadow);
        border: none;
        border-radius: 5px;
        padding: 5px 10px;
        cursor: pointer;
    }

    .buttons__item--active {
        background-color: var(--main);
        color: var(--white);
    }

    .buttons__item--active .tabs{
        color: var(--white);
        fill: var(--white);
    }

</style>
