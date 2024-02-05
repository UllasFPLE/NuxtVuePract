<template>
  <div class="w-full h-full flex flex-col justify-between items-center overflow-hidden">
    <footer v-motion :initial="InitialPos" :enter="EnterAnimation" :delay="400"
      class="w-full flex-grow h-[200px] sm:h-[300px] md:h-[500px] sm:p-[40px] flex justify-center items-center flex-col">
      <h1 class="text-[30px] sm:text-[38px] md:text-[48px] xl:text-[72px] font-medium text-nowrap text-black ">Let's work
        together.
      </h1>
      <nuxt-link
        class="text-[30px] sm:text-[38px] md:text-[42px] xl:text-[72px] text-nowrap text-[#7f7f7f] transition-all duration-150 hover:text-[#7f7f7f90]"
        to="https://www.linkedin.com/in/ullas-js-7694391b2/">Get in touch.</nuxt-link>
    </footer>
    <div class="w-full flex flex-col sm:flex-row justify-between">
      <div class="flex justify-center items-center gap-4 flex-col sm:flex-row mb-4 sm:m-0">
        <img class="animate-spin"
          src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABgAAAAYCAYAAADgdz34AAAAAXNSR0IArs4c6QAAAhlJREFUSEu11UmojmEUB/CfORtTYUMpybCgJAtFZEhJFtgIRSwQC0rCllJWEimJDAtJEglRQihliFgow86QMSyMz9Gh7977ffd7b12n3p53OM/5n+f8/+e8Xfxn6/Kf4+sIQHdcwjfMxvcqyXUEYDEOZ9C4P9rZAPcwNoPex7jOBJiGy/iYQftgKq40A6laojOYg53oWoDW4zTmdQbASDzCDwzLgC/4I5DheNoeSO0JpmeWgxDX4FwHohuOYEkGC4IXJehrvMLLmvVslrSFTD8galvPfiXBD/JjkH0ny1XPP0AjyRYAq8rLPel9ERsQoO9ryG0drC/6IU55CGMQySzL5zaNthz7E3g31jYjEb1xCrPwBQtw7u++eipaiGOIzm0GEtmfx0REWQLkbm1SjWQa8juRIKsL4XsbnORWBn+CmXjW2q+9Pojs12BbmTtbGwCEXIeWGTUZ1+r5tAdwHZMwF9Fo9exAEhoJRCJtrBFAr6KiT2VTDwzAO4zGPvzECkRZgq/juFp0P6UjAJF5nOBhGQnjy4jegk3omUG+ZtkO4k2ChmQ/V+VgY5HfjjL3b6bOR+XGXbmuy/VGkfWQ5GF+acaTVQFikEXt/1rMoqW4nS8mpJRH1PhE/6ysChBzJVo9/l5B3va8r90f5dqc5YueeV4zDP/5NSL5AvrncHvcpJuD/Bh+b4tUZ1Q9QZOY1T9X/eFUj9jK8zdOV2IZ6b9nygAAAABJRU5ErkJggg==" />
        © Ullas Js 2023
      </div>
      <div class="flex justify-center items-center gap-6 font-[Neue Montreal]">
        <nuxt-link to="https://www.instagram.com/ullax_js_/">Instagram</nuxt-link>
        <nuxt-link to="https://www.linkedin.com/in/ullas-js-7694391b2/">Linkedin</nuxt-link>
        <nuxt-link to="/">Mail</nuxt-link>
      </div>
    </div>
  </div>
</template>

<script setup>

const InitialPos = { opacity: 0, y: 100 }

const EnterAnimation = {
  opacity: 1, y: 0,
  transition: {
    duration: 400,
    ease: 'easeOut',
    type: 'spring',
    stiffness: 250,
    damping: 25,
    mass: 0.5,
  }
}

</script>