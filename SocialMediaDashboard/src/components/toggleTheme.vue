<template>
    <div id="toggle-button">
        <p id="dark-text">Dark Mode</p>
        <label class="switch">
        <input type="checkbox" v-model="isDarkMode" @change="toggleDarkMode">
        <span class="slider"></span>
        </label>
    </div>
</template>

<script setup>
    import { defineEmits,ref } from 'vue';

    const isDarkMode = ref(true);
    const emit = defineEmits(["toggle-dark-mode"]);

    const toggleDarkMode = () => { // Toggle the state
    emit("toggle-dark-mode", isDarkMode.value); // Emit the new state
    }
</script>

<style scoped>

    #toggle-button {
        width: 100%;
        display: flex;
        flex-direction: row;
        margin-left: 5%;
    }

    #dark-text {
        position: relative;
        top: -13px;
        font-weight: 700;
        color: hsl(228, 34%, 66%);
    }

    .switch {
    position: relative;
    display: inline-block;
    width: 50px;
    height: 25px;
    margin-left: auto;
    margin-right: 10%;
    }

    .switch input {
    opacity: 0;
    width: 0;
    height: 0;
    }

    .slider {
    position: absolute;
    cursor: pointer;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: #ccc;
    transition: .4s;
    border-radius: 20px;
    }

    .slider:before {
    position: absolute;
    content: "";
    height: 20px;
    width: 20px;
    left: 4px;
    bottom: 3px;
    background-color: white;
    transition: .4s;
    border-radius: 50%;
    }

    input:checked + .slider {
    background-color: black;
    }

    input:checked + .slider:before {
    transform: translateX(23px);
    }

    .slider.round {
    border-radius: 50%;
    }

    .slider.round:before {
    border-radius: 50%;
    }

    @media(min-width:500px) {
        #dark-text {
            margin-left: auto;
            margin-right: 1%;
        }

        .switch {
            margin-left: 0;
        }
    }
</style>
