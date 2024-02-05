<template>
  <div class="w-full flex flex-col">
    <header
      class="fixed z-20 top-0 w-full flex justify-center items-center px-[20px] py-[20px] md:px-[30px] md:py-[40px]">
      <div class="relative">
        <div class="bg-[#e8e5e480] flex gap-3 rounded-full overflow-hidden">
          <nuxt-link class="p-[15px] hover:bg-black hover:text-white transition-all duration-300 material-icons !blur-0 hover:scale-110 flex justify-center items-center" to="/">
            <i class="material-icons">close</i>
          </nuxt-link>
        </div>
        <div class="blur-background absolute inset-0 -z-10 rounded-full"></div>
      </div>
    </header>
    <div class=" p-[10px] sm:p-[20px] md:p-[40px] min-h-svh flex justify-center items-start"
      :class="{ '!mt-0 !h-screen flex flex-col justify-between items-center': isContactPage }">
      <slot />
    </div>
  </div>
</template>

<script setup>

</script>

<style scoped>
.blur-background {
  backdrop-filter: blur(8px);
  /* Adjust the blur intensity as needed */
}
</style>