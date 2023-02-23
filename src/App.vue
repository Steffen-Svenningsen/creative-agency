<template>
  <header>
    <router-link class="logo" to="/">Creators</router-link>
    <nav>
      <router-link to="/">Projects</router-link>
      <router-link to="/">About</router-link>
      <router-link to="/">Charity</router-link>
      <router-link class="contact" to="/">Contact</router-link>
    </nav>
  </header>
  <RouterView />
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

    .contact
      background-color: $honey-gold
      padding: 0.5rem 1rem
      border-radius: 4px

      &:hover
        color: $black
        transform: scale(1.05)
</style>