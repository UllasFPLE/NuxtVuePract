<template>
  <div class="w-full flex flex-col">
    <header class="fixed z-20 top-0 w-full flex justify-center items-center px-[20px] py-[20px] md:px-[30px] md:py-[40px]"
      >
      <div class="relative">
        <div class="bg-[#e8e5e480] flex gap-3 rounded-full overflow-hidden p-[5px]">
          <nuxt-link class="links !blur-0" to="/">Home</nuxt-link>
          <nuxt-link class="links !blur-0" to="/profile">Profile</nuxt-link>
          <nuxt-link class="links !blur-0" to="/contact">Contact</nuxt-link>
        </div>
        <div class="blur-background absolute inset-0 -z-10 rounded-full"></div>
      </div>
    </header>
    <div class=" p-[10px] sm:p-[20px] md:p-[40px] min-h-svh sm:mt-20" :class="{ '!mt-0 !h-screen flex flex-col justify-between items-center': isContactPage }">
      <slot />
    </div>
  </div>
</template>

<script setup>
const route = useRoute();
const isContactPage = computed(() => route.path == '/contact');
</script>

<style scoped>
.blur-background {
  backdrop-filter: blur(8px);
  /* Adjust the blur intensity as needed */
}

.links {
  font-size: 16px;
  font-family: "Neue Montreal Regular", sans-serif;
  font-weight: 500;
  @apply px-[25px] py-[10px] sm:px-[30px] sm:py-[10px];
  border-radius: 50px;
  color: #000;
}

.router-link-exact-active {
  @apply bg-white transition-all duration-300
}
</style>