<script setup>
import { ref } from "vue";

const mobileNav = ref(false);
</script>

<template>
    <button @click="mobileNav = !mobileNav" class="hamburger">
        <div class="line"></div>
        <div class="line"></div>
    </button>
    <div v-show="mobileNav" class="mobile-nav">
        <router-link @click="mobileNav = !mobileNav" to="/">Home</router-link>
        <router-link @click="mobileNav = !mobileNav" to="/projects">Projects</router-link>
        <router-link @click="mobileNav = !mobileNav" to="/about">About</router-link>
        <router-link @click="mobileNav = !mobileNav" to="/charity">Charity</router-link>
        <router-link @click="mobileNav = !mobileNav" to="/contact">Contact</router-link>
    </div>
</template>

<style lang="sass" scoped>
@import @/assets/main.sass

.hamburger
    outline: none
    background: none
    border: none
    display: none
    justify-content: center
    align-items: center
    flex-direction: column
    width: 24px
    height: 24px
    gap: 0.3rem
    cursor: pointer
    box-sizing: border-box

    .line
        width: 24px
        height: 2px
        background-color: $honey-gold

        &:last-of-type
            width: 18px
            align-self: flex-start

.mobile-nav
    position: fixed
    height: 100%
    width: 100%
    background-color: $honey-gold
    display: flex
    flex-direction: column
    gap: 5%
    box-sizing: border-box
    top: 0
    left: 0
    justify-content: center
    align-items: center
    overflow-y: hidden
    z-index: 100

    a
        font-family: "Anek Malayalam", sans-serif
        font-size: clamp(52px, 15vw, 104px)
        text-decoration: none
        color: $sand

@media (max-width: 700px)
    .hamburger
        display: flex            
</style>