<template>
  <main>
    <section class="hero-section">
      <div class="hero-line">
        <div class="hero-image h-top"></div>
        <h1 class="bold">Creative Agency</h1>
      </div>
      <div class="hero-line">
        <h1>for the</h1>
        <div class="hero-image h-mid"></div>
      </div>
      <div class="hero-line">
        <div class="hero-image h-bottom"></div>
        <h1 class="bold">People</h1>
      </div>
    </section>
    <section class="start-section">
      <h3 class="title-left bold"><span class="gold">Unlimited</span> <br>possibilities. <br> Join the people.</h3>
      <img src="../../public/website.webp" alt="Website">
      <img src="../../public/webshop.webp" alt="Webshop">
      <img src="../../public/meeting.webp" alt="Meeting">
      <div class="text-right">
        <p>With 15 years of experience regarding web-design and development We seek to create performance optimized digital solutions that are ready to grow to their full potential.</p>
      </div>
      <a class="cta" href="#">Start Your Journey Today<span class="gold">!</span></a>
    </section>
  </main>
</template>

<style lang="sass" scoped>
@import @/assets/main.sass

main
  width: 100%
  height: 100%

  section
    display: flex

  .hero-section
    flex-direction: column
    width: 100%
    height: 100vh
    background-color: $sand
    background-image: url("../../public/hero-background.png")
    background-size: cover
    align-items: center
    gap: 2rem

    .hero-line
      display: flex
      align-items: center
      gap: 2rem
      width: 100%
      transition: 0.3s
      transition-delay: 0.1s 
      cursor: default

      &:hover
        transform: scale(1.025)

      .bold
        font-weight: bold

      .hero-image
        background-position: center
        background-size: cover
        
      .h-top
        background-image: url("../../public/hero-small.webp")
        height: clamp(120px, 10vh, 240px)
        width: 20%
        border-radius: 100px

      .h-mid
        background-image: url("../../public/hero-top.webp")
        height: clamp(120px, 10vh, 240px)
        width: 70%
        border-radius: 100px 0 100px 100px

      .h-bottom
        background-image: url("../../public/hero-bottom.webp")
        height: clamp(120px, 10vh, 240px)
        width: 70%
        border-radius: 0 100px 100px 0

  .start-section
    background-color: $sand
    flex-direction: column
    position: relative
    height: 100vh
    width: 100%
    overflow-x: hidden

    .title-left
      position: absolute
      bottom: 8%
      left: 2rem
    .text-right
      width: clamp(200px, 30%, 600px)
      position: absolute
      right: 2rem
      top: 0
      opacity: 0.50

    .cta
      position: absolute
      bottom: 13%
      right: 2rem
      color: $black
      font-weight: bold
      font-family: "Anek Malayalam", sans-serif

    img
      width: clamp(300px, 25%, 600px)
      height: auto
      position: absolute
      transition: 0.2s

      &:nth-of-type(1)
        top: 50%
        left: 50%
        transform: translate(-50%,-50%)

      &:nth-of-type(2)
        top: 50%
        left: 50%
        transform: translate(-110%,-110%)
        border-radius: 0 0 100px 0

      &:nth-of-type(3)
        top: 50%
        left: 50%
        transform: translate(10%,10%)
        border-radius: 100px 0 0 0
</style>