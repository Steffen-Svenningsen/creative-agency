<template>
    <button class="hamburger">
        <div class="line"></div>
        <div class="line"></div>
    </button>
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

@media (max-width: 700px)
    .hamburger
        display: flex            
</style>