<script setup>
    import IconText from '../components/IconText.vue';
    import Account from '../components/icons/Account.vue';
    import Check from '../components/icons/Check.vue';
    import Country from '../components/icons/Country.vue';
    import Language from '../components/icons/Language.vue';
    import Phone from '../components/icons/Phone.vue';
    import Message from '../components/icons/Message.vue';
    import Mail from '../components/icons/Mail.vue';

    const name = 'John Doe';
    const status = 'Active';
    const country = 'COL';
    const language = 'EN';
    const contact = '(123) 555-5555';
    const nick = 'johndoe123';
    const email = 'johndoe123@example.com';
</script>

<template>
    <div class="profile">
        <div class="about">
            <div class="about__field">
                <h4>ABOUT</h4>
                <IconText>
                    <Account class="icon"/>
                    Full Name: {{ name }}
                </IconText>
                <IconText>
                    <Check class="icon"/>
                    Status: {{ status }}
                </IconText>
                <IconText>
                    <Country class="icon"/>
                    Country: {{ country }}
                </IconText>
                <IconText>
                    <Language class="icon"/>
                    Language: {{ language }}
                </IconText>
            </div>
            <div class="about__field">
                <h4>Contacts</h4>
                <IconText>
                    <Phone class="icon"/>
                    Contact: {{ contact }}
                </IconText>
                <IconText>
                    <Message class="icon"/>
                    Skype: {{ nick }}
                </IconText>
                <IconText>
                    <Mail class="icon"/>
                    Email: {{ email }}
                </IconText>
            </div>
            <div class="about__field">
                <h4>teams</h4>
                <p>Backend Developer (126 Members)</p>
                <p>VueJS Developer (86 Members)</p>
            </div>
        </div>
        <div class="activity">

        </div>
    </div>
</template>


<style scoped>
    .profile {
        width:  100%;
        display: flex;
        justify-content: start;
        align-items: start;
        height: 100%;
    }

    .about{
        display: flex;
        justify-content: start;
        align-items: start;
        gap: 10px;
        flex-direction: column;
        height: min-content;
        width: min-content;
        padding: 2%;
        color: var(--shadow);
        background-color: var(--white);
        border-radius: 5px;
        box-shadow: 0 0 .5rem var(--shadow);
    }

    .about__field{
        display: flex;
        flex-direction: column;
        gap: 5px;
    }
    
    .about__field h4{
        font-size: .9rem;
        text-transform: uppercase;
    }

    .about__field p{
        font-size: .8rem;
        color: var(--gray);
    }
</style>