<script setup lang="ts">
    import { ref, computed, markRaw } from 'vue';
    import Banner from "./components/Banner.vue";
    import Navbar from "./components/Navbar.vue";

    import Profile from "./views/Profile.vue";
    import Teams from "./views/Teams.vue";
    import IconText from "./components/IconText.vue";
    import Account from "./components/icons/Account.vue";
    import Team from "./components/icons/Team.vue";

    // Mark the components as non-reactive
    const AccountRaw = markRaw(Account);
    const TeamRaw = markRaw(Team);

    const tabs = ref([
        { name: "Profile", icon: AccountRaw, styleType: 'tabs' },
        { name: "Teams", icon: TeamRaw, styleType: 'tabs' }
    ]);

    const activeComponent = ref('Profile');

    const componentMap = {
        Profile,
        Teams
    };

    const currentComponent = computed(() => componentMap[activeComponent.value]);

</script>

<template>

    <Navbar/>
    

    <Banner/>

    <div class="buttons">
        <button 
        v-for='tab in tabs' 
        :key='tab.name' 
        @click='activeComponent = tab.name'
        :class="{'buttons__item': true, 'buttons__item--active': tab.name === activeComponent}" 
        >
            <IconText :styleType="tab.styleType">
                <component :is="tab.icon" class="icon"/>
                {{ tab.name }}
            </IconText>
        </button>
    </div>

  <component :is="currentComponent"/>

</template>

<style >

    body{
        display: flex;
        justify-content: center;
        background-color: var(--base);
        scroll-behavior: smooth;
    }

    .app{
        padding: 1.3rem 0;
        width: 95vw;
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: start;
        flex-direction: column;
        gap: 1.3rem;
    }

    .buttons{
        display: flex;
        justify-content: start;
        align-items: center;
        gap: 20px;
        width: 100%;
    }

    .buttons__item{
        transition: all 0.2s ease;
        background-color: transparent;
        border: none;
        border-radius: var(--border);
        padding: 8px 20px;
        cursor: pointer;
        color: var(--accent);
    }

    .buttons__item--active {
        background-color: var(--slate);
        color: var(--accent);
    }

    .buttons__item--active .tabs{
        color: var(--base);
        fill: var(--base);
    }

</style>
