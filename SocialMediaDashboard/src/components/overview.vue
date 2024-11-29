<template>
    <main>
        <h1 class="overview" :class="{'dark-mode-text': isDarkMode, 'light-mode-text': !isDarkMode}">Overview - Today</h1>
        <div class="cards">
            <div class="overview-card" :class="{'dark-mode': isDarkMode, 'light-mode': !isDarkMode}" >
                <div class="overview-top">
                    <p class="top-text">Page views</p>
                    <img src="../../public/images/icon-facebook.svg" alt="" class="logo">
                </div>
                <div class="overview-bot">
                    <p class="bot-text-counter" :class="{'dark-mode-text-count': isDarkMode, 'light-mode-text-count': !isDarkMode}">87</p>
                    <img src="../../public/images/icon-up.svg" alt="" class="up">
                    <p class="bot-percentage">3%</p>
                </div>
            </div>

            <div class="overview-card" :class="{'dark-mode': isDarkMode, 'light-mode': !isDarkMode}">
                <div class="overview-top">
                    <p class="top-text">Likes</p>
                    <img src="../../public/images/icon-facebook.svg" alt="" class="logo">
                </div>
                <div class="overview-bot">
                    <p class="bot-text-counter" :class="{'dark-mode-text-count': isDarkMode, 'light-mode-text-count': !isDarkMode}">52</p>
                    <img src="../../public/images/icon-down.svg" alt="" class="up">
                    <p class="bot-percentage">2%</p>
                </div>
            </div>

            <div class="overview-card" :class="{'dark-mode': isDarkMode, 'light-mode': !isDarkMode}">
                <div class="overview-top">
                    <p class="top-text">Likes</p>
                    <img src="../../public/images/icon-instagram.svg" alt="" class="logo">
                </div>
                <div class="overview-bot">
                    <p class="bot-text-counter" :class="{'dark-mode-text-count': isDarkMode, 'light-mode-text-count': !isDarkMode}">5462</p>
                    <img src="../../public/images/icon-up.svg" alt="" class="up">
                    <p class="bot-percentage">2257%</p>
                </div>
            </div>

            <div class="overview-card" :class="{'dark-mode': isDarkMode, 'light-mode': !isDarkMode}">
                <div class="overview-top">
                    <p class="top-text">Profile views</p>
                    <img src="../../public/images/icon-instagram.svg" alt="" class="logo">
                </div>
                <div class="overview-bot">
                    <p class="bot-text-counter" :class="{'dark-mode-text-count': isDarkMode, 'light-mode-text-count': !isDarkMode}">52K</p>
                    <img src="../../public/images/icon-up.svg" alt="" class="up">
                    <p class="bot-percentage">1375%</p>
                </div>
            </div>

            <div class="overview-card" :class="{'dark-mode': isDarkMode, 'light-mode': !isDarkMode}">
                <div class="overview-top">
                    <p class="top-text">Retweets</p>
                    <img src="../../public/images/icon-twitter.svg" alt="" class="logo">
                </div>
                <div class="overview-bot">
                    <p class="bot-text-counter" :class="{'dark-mode-text-count': isDarkMode, 'light-mode-text-count': !isDarkMode}">117</p>
                    <img src="../../public/images/icon-up.svg" alt="" class="up">
                    <p class="bot-percentage">303%</p>
                </div>
            </div>

            <div class="overview-card" :class="{'dark-mode': isDarkMode, 'light-mode': !isDarkMode}">
                <div class="overview-top">
                    <p class="top-text">Likes</p>
                    <img src="../../public/images/icon-twitter.svg" alt="" class="logo">
                </div>
                <div class="overview-bot">
                    <p class="bot-text-counter" :class="{'dark-mode-text-count': isDarkMode, 'light-mode-text-count': !isDarkMode}">507</p>
                    <img src="../../public/images/icon-up.svg" alt="" class="up">
                    <p class="bot-percentage">553%</p>
                </div>
            </div>

            <div class="overview-card" :class="{'dark-mode': isDarkMode, 'light-mode': !isDarkMode}">
                <div class="overview-top">
                    <p class="top-text">Likes</p>
                    <img src="../../public/images/icon-youtube.svg" alt="" class="logo">
                </div>
                <div class="overview-bot">
                    <p class="bot-text-counter" :class="{'dark-mode-text-count': isDarkMode, 'light-mode-text-count': !isDarkMode}">107</p>
                    <img src="../../public/images/icon-down.svg" alt="" class="up">
                    <p class="bot-percentage">19%</p>
                </div>
            </div>

            <div class="overview-card" :class="{'dark-mode': isDarkMode, 'light-mode': !isDarkMode}">
                <div class="overview-top">
                    <p class="top-text">Total views</p>
                    <img src="../../public/images/icon-facebook.svg" alt="" class="logo">
                </div>
                <div class="overview-bot">
                    <p class="bot-text-counter" :class="{'dark-mode-text-count': isDarkMode, 'light-mode-text-count': !isDarkMode}">1407</p>
                    <img src="../../public/images/icon-up.svg" alt="" class="up">
                    <p class="bot-percentage">12%</p>
                </div>
            </div>

        </div>
    </main>
</template>

<script setup>
    import { defineProps } from 'vue';

    const props = defineProps({
        isDarkMode: Boolean,
    })
</script>

<style scoped>
    .overview {
        margin-left: 5%;
        font-weight: bold;
    }

    .dark-mode-text {
        color: white;
    }

    .light-mode-text {
        color: black;
    }

    .overview-card {
        display: flex;
        flex-direction: column;
        margin-left: 5%;
        width: 87%;
        margin-bottom: 3%;
        border-radius: 20px;
        padding: 0px 0px 10px 10px;
    }

    .dark-mode {
        background-color: hsl(228, 28%, 20%);
    }

    .light-mode {
        background-color: hsl(227, 47%, 96%);
    }

    .overview-top {
        display: flex;
        flex-direction: row;
        width: 100%;
        align-items: center;
    }

    .top-text {
        color: hsl(228, 34%, 66%);
        font-weight: 700;
    }

    .logo {
        margin-left: auto;
        margin-right: 5%;
    }

    .overview-bot {
        width: 100%;
        display: flex;
        flex-direction: row;
        align-items: center;
    }

    .bot-text-counter {
        font-size: 40px;
        font-weight: 700;
        margin-top: -3%;
        
    }

    .dark-mode-text-count {
        color: white;
    }

    .light-mode-text-count {
        color: black;
    }

    .up {
        margin-left: auto;
        margin-top: -15%;
        margin-right: 2%;
    }

    .bot-percentage {
        margin-top: -10%;
        margin-right: 2%;
        color: hsl(0, 0%, 40%);
        font-weight: 700;
    }

    @media(min-width:500px){
        .overview {
            margin-left: 2%;
        }

        .cards {
            width: 100%;
            display: flex;
            flex-direction: row;
            flex-wrap: wrap;
            margin-left: 1%;
        }

        .overview-card{
            width: 22.5%;
            margin-left: 1%;
        }

        .overview-bot {
            margin-top: 5%;
        }

        .bot-text-counter {
            margin-top: 0;
        }
    }
</style>