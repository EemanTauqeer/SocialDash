<template>
  <div :class="{'dark-mode': isDarkMode, 'light-mode': !isDarkMode}" class="main">
    <div :class="{'top-dark': isDarkMode, 'top-light': !isDarkMode}" class="top">
      <div class="top-text">
        <h2 :class="{'dashboard-title': isDarkMode, 'dashboard-title-light': !isDarkMode}">Social Media Dashboard</h2>
        <p class="total-followers">Total Followers: 23,004</p>
      </div>
      <hr id="line">
      <toggleTheme :isDarkMode = "isDarkMode" @toggle-dark-mode="toggleDarkMode" class="toggle-mobile"/>
    </div>
      <topCard class="top-card" :isDarkMode="isDarkMode"/>
      <overview :isDarkMode="isDarkMode" class="overview"/>
  </div>
</template>

<script setup>
  import toggleTheme from './components/toggleTheme.vue';
  import topCard from './components/topCard.vue';
  import overview from './components/overview.vue';
  import { ref } from 'vue';

  const isDarkMode = ref(true);
  const toggleDarkMode = (newValue) => {
    isDarkMode.value = newValue;
  }
</script>


<style scoped>

  html {
      font-family: "Inter", sans-serif;
  }

  .main {
    display: flex;
    flex-direction: column;
    width: 400px;
    background-color: hsl(230, 17%, 14%);
    margin-top: -2%;
  }

  .dark-mode {
    background-color: hsl(230, 17%, 14%);
  }

  .light-mode {
    background-color: hsl(0, 0%, 100%);
  }

  .top {
    width: 400px;
    padding-bottom: 40px;
    border-radius: 0 0 20px 20px;
  }

  .top-dark {
    background-color: hsl(231, 27%, 19%);
  }

  .top-light {
    background-color: hsl(220, 8%, 85%);
  }

  .top-card {
    position: relative;
    top: -30px;
  }

  .top-text {
    width: 400px;
    display: flex;
    flex-direction: column;
  }

  .dashboard-title {
    font-size: 25px;
    font-weight: 700;
    color: white;
    margin-left: 5%
  }

  .dashboard-title-light {
    font-size: 25px;
    font-weight: 700;
    color: black;
    margin-left: 5%
  }

  .total-followers {
    font-size: 17px;
    margin-left: 5%;
    margin-top: -3%;
    color: hsl(163, 72%, 41%);
    font-weight: 700;
  }

  #line {
    width: 90%;
  }

  @media(min-width:500px) {
    .main {
      width: 100%;
      margin-top: 0;
      overflow: hidden;
    } 

    #line {
      display: none;
    }

    .top {
      width: 100%;
      display:flex;
      flex-direction: row;
      padding-bottom: 100px;
    }

    .toggle-mobile {
      display: flex;
      flex-direction: row;
      margin-top: 2%;
    }

    .top-card {
      width: 100%;
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      margin-top: -3%;
    }

    .top-text {
      margin-left: 1%;
      width: 50%;
    }

    .overview {
      display: flex;
      flex-direction: column;
      width: 100%;
      margin-left: 0;
      margin-top: -3%;
    }
  }
</style>
