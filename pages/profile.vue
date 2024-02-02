<template>
  <div class="w-full flex flex-col min-h-svh">
    <section class="w-full h-[400px] p-[20px] sm:p-[40px] md:h-[600px] flex justify-center items-center">
      <h1 class="text-[36px] text-nowrap font-[Neue Montreal] font-semibold sm:text-[48px] md:text-[72px]">Hey 👋🏼 I'm
        Ullas</h1>
    </section>
    <section class="w-full flex justify-center items-center gap-10 px-5 md:px-28">
      <div class="w-full min-h-[300px] sm:h-[500px] overflow-hidden flex-1 rounded-2xl shadow-xl">
        <img src="/assets/images/1.png" alt="">
      </div>
      <div class="hidden xl:block w-full h-[500px] overflow-hidden flex-1 rounded-2xl shadow-xl">
        <img src="/assets/images/2.png" alt="">
      </div>
    </section>
    <section class="pt-[60px] sm:px-[20px] sm:pb-[20px] flex flex-col justify-center items-center gap-5">
      <p class="text-[14px] px-[12px] py-[8px] bg-[#e8e5e480] rounded-3xl text-black font-[Neue Montreal]">About</p>
      <h3 class="text-[24px] font-medium font-[Neue Montreal] text-center md:text-[38px] max-w-[700px]">
        A freelance designer based in India. I combine my experience in product and brand to solve problems, tell
        stories, and create creative web designs.
      </h3>
    </section>
    <section class="pt-[80px] px-[40px] pb-[40px] flex flex-col justify-center items-center gap-5">
      <p class="text-[14px] px-[12px] py-[8px] bg-[#e8e5e480] rounded-3xl text-black font-[Neue Montreal]">Experience</p>
      <h3 class="text-[24px] text-nowrap font-medium font-[Neue Montreal] text-center md:text-[38px] max-w-[700px]">
       Where I've worked
      </h3>
    </section>

    <Footer />
  </div>
</template>