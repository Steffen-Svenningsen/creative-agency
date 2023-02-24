<script setup>
import HamburgerMenu from "@/components/HamburgerMenu.vue";
</script>

<template>
  <header>
    <router-link class="logo" to="/">Creators</router-link>
    <nav>
      <router-link to="/projects">Projects</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/charity">Charity</router-link>
      <router-link class="contact" to="/contact">Contact</router-link>
    </nav>
    <HamburgerMenu />
  </header>
  <router-view v-slot="{ Component }">
    <transition name="fade" mode="out-in">
      <component :is="Component" />
    </transition>
  </router-view>
  <footer>
    <div>
      <h3>Address</h3>
      <span><a href="#">Sandgravvej 12</a></span>
      <span>8200 Aarhus N</span>
    </div>
    <div>
      <h3>Contact</h3>
      <span>E-mail:<a href="#"> info@creators.dk</a></span>
      <span>Phone:<a href="#"> +45 12 34 56 78</a></span>
    </div>
    <div>
      <h3>Shortcuts</h3>
      <span><router-link to="/projects">Projects</router-link></span>
      <span><router-link to="/about">About</router-link></span>
      <span><router-link to="/charity">Charity</router-link></span>
      <span><router-link to="/contact">Contact</router-link></span>
    </div>
  </footer>
</template>

<style lang="sass" scoped>
@import @/assets/main.sass

header
  display: flex
  justify-content: space-between
  align-items: center
  padding: 2rem
  box-sizing: border-box
  background-color: $sand

  .logo
    font-family: "Anek Malayalam", sans-serif
    font-size: 2rem
    text-decoration: none
    color: $honey-gold

  nav
    display: flex
    gap: 1rem
    align-items: center

    a
      font-size: 1rem
      text-decoration: none
      color: $black
      font-family: "Roboto", sans-serif
      transition: 0.2s

      &:hover
        color: $honey-gold

    a.router-link-active
      color: $honey-gold
      border-bottom: 2px solid $honey-gold

      &:last-of-type
        color: $black
        border-bottom: none 

    .contact
      background-color: $honey-gold
      padding: 0.5rem 1rem
      border-radius: 4px

      &:hover
        color: $black
        transform: scale(1.05)

footer
  display: flex
  justify-content: space-between
  align-items: flex-end
  padding: 2rem
  box-sizing: border-box
  background-color: $sand
  height: 100%
  flex-wrap: wrap
  padding-top: 120px

  div
    display: flex
    flex-direction: column
    gap: 0.5rem
    min-width: 120px
    height: 200px

    h3
      font-size: clamp(28px, 4vw, 48px)
      font-family: "Anek Malayalam", sans-serif
      font-weight: 500
      text-decoration: underline solid $honey-gold
      margin-bottom: 1.5rem

    span
      font-family: "Roboto", sans-serif
      color: $black
      font-size: 22px

      a
        text-decoration: none
        color: $black
        transition: 0.2s

        &:hover
         color: $honey-gold

.fade-enter-from,
.fade-leave-to
  transform: translateX(-100%)

.fade-enter-active,
.fade-leave-active
  transition: 0.5s

@media (max-width: 700px)
  header
    nav
      display: none
</style>