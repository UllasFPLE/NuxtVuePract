<template>
  <div class="w-full flex flex-col min-h-svh">
    <section  class="w-full h-[400px] p-[20px] sm:p-[40px] md:h-[600px] flex justify-center items-center">
      <h1 v-motion :initial="InitialPos" :enter="EnterAnimation" :delay="400" class="text-[36px] text-nowrap font-[Neue Montreal] font-medium sm:text-[48px] md:text-[72px]">Hey 👋🏼 I'm
        Ullas</h1>
    </section>
    <section v-motion :initial="InitialPos" :enter="EnterAnimation1" :delay="500" class="w-full flex justify-center items-center gap-10 px-5 md:px-28">
      <div class="w-full min-h-[300px] sm:h-[500px] overflow-hidden flex-1 rounded-2xl shadow-xl">
        <img src="/assets/images/1.png" alt="">
      </div>
      <div class="hidden xl:block w-full h-[500px] overflow-hidden flex-1 rounded-2xl shadow-xl">
        <img src="/assets/images/2.png" alt="">
      </div>
    </section>
    <section v-motion :initial="InitialPos" :enter="EnterAnimation1" :delay="600" class="pt-[60px] sm:px-[20px] sm:pb-[20px] flex flex-col justify-center items-center gap-5">
      <p class="text-[14px] px-[12px] py-[8px] bg-[#e8e5e480] rounded-3xl text-black font-[Neue Montreal]">About</p>
      <h3 class="text-[24px] font-medium font-[Neue Montreal] text-center md:text-[38px] max-w-[700px]">
        A freelance designer based in India. I combine my experience in product and brand to solve problems, tell
        stories, and create creative web designs.
      </h3>
    </section>
    <section v-motion :initial="InitialPos" :enter="EnterAnimation1" :delay="700" class="pt-[80px] px-[40px] pb-[40px] flex flex-col justify-center items-center gap-5">
      <p class="text-[14px] px-[12px] py-[8px] bg-[#e8e5e480] rounded-3xl text-black font-[Neue Montreal]">Experience</p>
      <h3 class="text-[24px] text-nowrap font-medium font-[Neue Montreal] text-center md:text-[38px] max-w-[700px]">
        Where I've worked
      </h3>
    </section>
    <section v-motion :initial="InitialPos" :enter="EnterAnimation1" :delay="800" class="p-[20px] grid grid-cols-2 sm:grid-cols-3 md:px-[80px]">
      <div class="p-[40px] flex flex-col gap-8 justify-center items-center w-full">
        <div class="flex flex-col gap-2">
          <p class="font-[Neue Montreal] capitalize text-[14px] text-[#828282] text-center text-nowrap">2024 - present</p>
          <p class="font-[Neue Montreal] text-[18px] text-center text-nowrap">FPLE</p>
          <p class="font-[Neue Montreal] capitalize text-[14px] text-[#828282] text-center text-nowrap">Front End Dev</p>
        </div>
        <div>
          <p
            class="text-[14px] px-[12px] py-[8px] bg-[#e8e5e480] rounded-3xl text-black font-[Neue Montreal] text-nowrap">
            Front End
            Dev</p>
        </div>
      </div>
      <div class="p-[40px] flex flex-col gap-8 justify-center items-center w-full">
        <div class="flex flex-col gap-2">
          <p class="font-[Neue Montreal] capitalize text-[14px] text-[#828282] text-center text-nowrap">2023</p>
          <p class="font-[Neue Montreal] text-[18px] text-center text-nowrap">SciPy</p>
          <p class="font-[Neue Montreal] capitalize text-[14px] text-[#828282] text-center text-nowrap">React Dev</p>
        </div>
        <div>
          <p
            class="text-[14px] px-[12px] py-[8px] bg-[#e8e5e480] rounded-3xl text-black font-[Neue Montreal] text-nowrap">
            Freelance</p>
        </div>
      </div>
      <div class="p-[40px] flex flex-col gap-8 justify-center items-center w-full">
        <div class="flex flex-col gap-2">
          <p class="font-[Neue Montreal] capitalize text-[14px] text-[#828282] text-center text-nowrap">2022</p>
          <p class="font-[Neue Montreal] text-[18px] text-center text-nowrap">SciPy</p>
          <p class="font-[Neue Montreal] capitalize text-[14px] text-[#828282] text-center text-nowrap">Mern Stack Dev</p>
        </div>
        <div>
          <p
            class="text-[14px] px-[12px] py-[8px] bg-[#e8e5e480] rounded-3xl text-black font-[Neue Montreal] text-nowrap text-center">
            Intern</p>
        </div>
      </div>
    </section>
    <Footer />
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
const EnterAnimation1 = {
  opacity: 1, y: 0,
  transition: {
    duration: 600,
    ease: 'easeOut',
    type: 'spring',
    stiffness: 250,
    damping: 25,
    mass: 0.5,
  }
}

</script>