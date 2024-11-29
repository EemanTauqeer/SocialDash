<template>
    <main>
        <div  :class="{'dark-mode': isDarkMode, 'light-mode': !isDarkMode}" class="card">
            <div class="media-box">
                <img src="../../public/images/icon-facebook.svg" alt="" class="logo">
                <p class="username">@nathanf</p>
            </div>
            <div class="follower-box">
                <p :class="{'dark-mode-text': isDarkMode, 'light-mode-text': !isDarkMode}" class="follower-count">1987</p>
                <p class="followers-text">FOLLOWERS</p>
            </div>
            <div class="card-bot">
                <img src="../../public/images/icon-up.svg" alt="" class="up">
                <p class="increase">12 today</p>
            </div>
        </div>

        <div class="card" :class="{'dark-mode': isDarkMode, 'light-mode': !isDarkMode}">
            <div class="media-box">
                <img src="../../public/images/icon-twitter.svg" alt="" class="logo">
                <p class="username">@nathanf</p>
            </div>
            <div class="follower-box">
                <p class="follower-count" :class="{'dark-mode-text': isDarkMode, 'light-mode-text': !isDarkMode}">1044</p>
                <p class="followers-text">FOLLOWERS</p>
            </div>
            <div class="card-bot">
                <img src="../../public/images/icon-up.svg" alt="" class="up">
                <p class="increase">99 today</p>
            </div>
        </div>

        <div class="card" :class="{'dark-mode': isDarkMode, 'light-mode': !isDarkMode}">
            <div class="media-box">
                <img src="../../public/images/icon-instagram.svg" alt="" class="logo">
                <p class="username">@nathanf</p>
            </div>
            <div class="follower-box">
                <p class="follower-count" :class="{'dark-mode-text': isDarkMode, 'light-mode-text': !isDarkMode}">11K</p>
                <p class="followers-text">FOLLOWERS</p>
            </div>
            <div class="card-bot">
                <img src="../../public/images/icon-up.svg" alt="" class="up">
                <p class="increase">1099 today</p>
            </div>
        </div>

        <div class="card" :class="{'dark-mode': isDarkMode, 'light-mode': !isDarkMode}">
            <div class="media-box">
                <img src="../../public/images/icon-youtube.svg" alt="" class="logo">
                <p class="username">@nathanf</p>
            </div>
            <div class="follower-box">
                <p class="follower-count" :class="{'dark-mode-text': isDarkMode, 'light-mode-text': !isDarkMode}">8239</p>
                <p class="followers-text">FOLLOWERS</p>
            </div>
            <div class="card-bot">
                <img src="../../public/images/icon-down.svg" alt="" class="up">
                <p class="increase">144 today</p>
            </div>
        </div>
    </main>
</template>

<script setup >
    import { defineProps } from 'vue';
    const props = defineProps({
        isDarkMode : Boolean,
    })
</script>

<style scoped>

    .light-mode {
        background-color: hsl(227, 47%, 96%);
    }

    .dark-mode {
        background-color: hsl(228, 28%, 20%);
    }

    .card {
        display: flex;
        flex-direction: column;
        margin-left: 5%;
        width: 90%;
        align-items: center;
        justify-content: center;
        text-align: center;
        margin-bottom: 3%;
        border-radius: 10px;
    }

    .card:nth-child(1) {
        border-top: 5px hsl(208, 92%, 53%) solid;
    }

    .card:nth-child(2) {
        border-top: 5px hsl(203, 89%, 53%) solid;
    }

    .card:nth-child(3) {
        border-top: 5px hsl(37, 40%, 43%) solid;
    }

    .card:nth-child(4) {
        border-top: 5px hsl(348, 97%, 39%) solid;
    }

    .media-box {
        width: 100%;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center
    }

    .username {
        margin-left: 3%;
        color: hsl(228, 34%, 66%);
        font-weight: 700;
        font-size: 15px;
    }

    .follower-box {
        margin-top: -15%;
    }

    .follower-count {
        font-size: 52px;
        font-weight: bold;
        color: hsl(0, 0%, 100%);
    }

    .dark-mode-text {
        color: hsl(228, 34%, 66%);
    }

    .light-mode-text {
        color: black;
    }

    .followers-text {
        font-weight: 500;
        margin-top: -50%;
    }

    .card-bot {
        width: 100%;
        height: auto;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: center;
    }

    .increase {
        margin-left: 2%;
        color: hsl(228, 34%, 66%);
    }

    @media(min-width:500px) {
        .card {
            margin-left: 0%;
            width: 80%;
            margin-right: 2%;
        }

        .card:nth-child(1) {
            margin-left: 2%;
        }
    }
</style>