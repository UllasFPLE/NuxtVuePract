<template>
  <div class="home_page flex flex-col justify-center items-center">
    <section class="w-full h-[400px] sm:h-[400px] md:h-[600px] flex flex-col justify-center gap-16 items-center">
      <h1 class="text-[36px] max-w-[900px] font-[Neue Montreal] font-semibold text-center sm:text-[48px] md:text-[72px]">A
        brand and product designer working with clients globally</h1>
      <div class="hidden sm:flex gap-3">
        <p class="font-[Neue Montreal] text-[14px] px-[12px] py-[8px]">Expertise</p>
        <p class="font-[Neue Montreal] text-[14px] px-[12px] py-[8px] bg-[#e8e5e480] rounded-[50px] font-medium">Branding
        </p>
        <p class="font-[Neue Montreal] text-[14px] px-[12px] py-[8px] bg-[#e8e5e480] rounded-[50px] font-medium">Product
        </p>
        <p class="font-[Neue Montreal] text-[14px] px-[12px] py-[8px] bg-[#e8e5e480] rounded-[50px] font-medium">Design
          Systems</p>
      </div>
    </section>
    <section class="p-[10px] sm:p-[30px] sm:px-[60px] flex flex-col md:flex-row gap-9">
      <Imager image="https://framerusercontent.com/images/kfr022WaJ8YJUyZFmdwCB3pXhs.jpg?scale-down-to=1024" word="Ari" />
      <Imager image="https://framerusercontent.com/images/QVKFKT3dyGxloXfzzpurVKNMM6M.jpg?scale-down-to=1024"
        word="Correlated" />
    </section>
    <section class="p-[10px] sm:p-[30px] sm:px-[60px] flex flex-col md:flex-row gap-9">
      <Imager image="https://framerusercontent.com/images/AX9PukosNfGVcfXw3YapiYpl9g.jpg?scale-down-to=1024"
        word="Channel 5" />
      <Imager image="https://framerusercontent.com/images/BAXywubxN8sAhfJg3AgGgFI.jpg?scale-down-to=1024"
        word="Ronald Abram" />
    </section>
    <section class="p-[10px] sm:p-[30px] sm:px-[60px] flex flex-col md:flex-row gap-9">
      <Videor
        video="https://framerusercontent.com/modules/assets/XuzMZ3Z1QQHKltPqRjzGnsWs27M~Jq48dGctHPeHtnn90xE_Aem-3HQJB_aNVwfu2fao5Ok.mp4"
        word="Propeller" />
      <Imager image="https://framerusercontent.com/images/3WALBX7nnuG7p85CLjlVmWPDHw.jpg?scale-down-to=1024"
        word="Schuh" />
    </section>
    <section class="p-[10px] sm:p-[30px] sm:px-[60px] flex flex-col md:flex-row gap-9">
      <Imager image="https://framerusercontent.com/images/e3moUZXfgtjYQY4ILakIMaz4n7s.jpg" word="Papper Street" />
      <Videor
        video="https://framerusercontent.com/modules/assets/SGjFvgcbK7s4yKh0xwuNjriMNII~5SCIlrVv6SNR5PFMjsMv3qAIi3sYsG2gjdlB0qM-tng.mp4"
        word="OH, SUPPLY" />
    </section>
    <section class="p-[10px] sm:p-[30px] sm:px-[60px] flex flex-col md:flex-row gap-9">
      <Imager image="https://framerusercontent.com/images/aH1eUgCIIIrbJF7TUlaKAehoI.jpg?scale-down-to=1024" word="Monokel Eyewear" />
      <Imagesoon image="https://framerusercontent.com/images/UbS7rWmAwWxjtwM7oaWwRuGo.jpg?scale-down-to=1024" word="Lawtrades" />
    </section>
    <section class="p-[10px] sm:p-[30px] sm:px-[60px] flex flex-col md:flex-row gap-9">
      <Imagesoon image="https://framerusercontent.com/images/hQVBeiDNGU2TfeDJALuhawlcto.jpg?scale-down-to=1024" word="BaselWorld" />
      <Videor video="https://framerusercontent.com/modules/assets/NieGBlxBdgpz9QCHV5Aj89rWjVg~DPEeC0jYyBwx9c865cOkUi-KzBM-3ukyhpgtPhvYo_U.mp4" 
      word="NYCB"
      />
    </section>
    <section class="w-full h-[200px] sm:h-[300px] md:h-[500px] sm:p-[40px] mt-[100px] flex justify-center items-center flex-col">
      <h1 class="font-[Neue Montreal] text-[30px] sm:text-[38px] md:text-[45px] text-nowrap text-black ">Let's work together.</h1>
      <nuxt-link class="text-[30px] sm:text-[38px] md:text-[42px] font-[Neue Montreal] text-nowrap text-[#7f7f7f] transition-all duration-150 hover:text-[#7f7f7f90]" to="/contact">Get in touch</nuxt-link>
    </section>
  </div>
</template>

<script setup>


</script>

<style scoped></style>
