<template>
  <div class="home_page flex flex-col justify-center items-center">
    <section class="w-full h-[400px] sm:h-[400px] md:h-[600px] flex flex-col justify-center gap-16 items-center">
      <h1 class="text-[36px] max-w-[900px] font-medium text-center sm:text-[48px] md:text-[72px]" v-motion
        :initial="InitialPos" :enter="EnterAnimation" :delay="500">A
        brand and product designer working with clients globally</h1>
      <div v-motion :initial="InitialPos" :enter="EnterAnimation1" :delay="600" class="hidden sm:flex gap-3">
        <p class="font-[Neue Montreal] text-[14px] px-[12px] py-[8px]">Expertise</p>
        <p class="font-[Neue Montreal] text-[14px] px-[12px] py-[8px] bg-[#e8e5e480] rounded-[50px]">Branding
        </p>
        <p class="font-[Neue Montreal] text-[14px] px-[12px] py-[8px] bg-[#e8e5e480] rounded-[50px]">Product
        </p>
        <p class="font-[Neue Montreal] text-[14px] px-[12px] py-[8px] bg-[#e8e5e480] rounded-[50px]">Design
          Systems</p>
      </div>
    </section>
    <section v-motion :initial="InitialPos" :enter="EnterAnimation1" :delay="700" class="p-[10px] sm:p-[30px] sm:px-[60px] flex flex-col md:flex-row gap-9">
      <LazyImager image="https://framerusercontent.com/images/kfr022WaJ8YJUyZFmdwCB3pXhs.jpg?scale-down-to=1024"
        word="Ari" />
      <LazyImager image="https://framerusercontent.com/images/QVKFKT3dyGxloXfzzpurVKNMM6M.jpg?scale-down-to=1024"
        word="Correlated" />
    </section>
    <section v-motion :initial="InitialPos" :enter="EnterAnimation1" :delay="800" class="p-[10px] sm:p-[30px] sm:px-[60px] flex flex-col md:flex-row gap-9">
      <LazyImager image="https://framerusercontent.com/images/AX9PukosNfGVcfXw3YapiYpl9g.jpg?scale-down-to=1024"
        word="Channel 5" />
      <LazyImager image="https://framerusercontent.com/images/BAXywubxN8sAhfJg3AgGgFI.jpg?scale-down-to=1024"
        word="Ronald Abram" />
    </section>
    <section v-motion :initial="InitialPos" :enter="EnterAnimation1" :delay="900" class="p-[10px] sm:p-[30px] sm:px-[60px] flex flex-col md:flex-row gap-9">
      <LazyVideor
        video="https://framerusercontent.com/modules/assets/XuzMZ3Z1QQHKltPqRjzGnsWs27M~Jq48dGctHPeHtnn90xE_Aem-3HQJB_aNVwfu2fao5Ok.mp4"
        word="Propeller" />
      <LazyImager image="https://framerusercontent.com/images/3WALBX7nnuG7p85CLjlVmWPDHw.jpg?scale-down-to=1024"
        word="Schuh" />
    </section>
    <section v-motion :initial="InitialPos" :enter="EnterAnimation1" :delay="1000" class="p-[10px] sm:p-[30px] sm:px-[60px] flex flex-col md:flex-row gap-9">
      <LazyImager image="https://framerusercontent.com/images/e3moUZXfgtjYQY4ILakIMaz4n7s.jpg" word="Papper Street" />
      <LazyVideor
        video="https://framerusercontent.com/modules/assets/SGjFvgcbK7s4yKh0xwuNjriMNII~5SCIlrVv6SNR5PFMjsMv3qAIi3sYsG2gjdlB0qM-tng.mp4"
        word="OH, SUPPLY" />
    </section>
    <section v-motion :initial="InitialPos" :enter="EnterAnimation1" :delay="1100" class="p-[10px] sm:p-[30px] sm:px-[60px] flex flex-col md:flex-row gap-9">
      <LazyImager image="https://framerusercontent.com/images/aH1eUgCIIIrbJF7TUlaKAehoI.jpg?scale-down-to=1024"
        word="Monokel Eyewear" />
      <LazyImagesoon image="https://framerusercontent.com/images/UbS7rWmAwWxjtwM7oaWwRuGo.jpg?scale-down-to=1024"
        word="Lawtrades" />
    </section>
    <section v-motion :initial="InitialPos" :enter="EnterAnimation1" :delay="1200" class="p-[10px] sm:p-[30px] sm:px-[60px] flex flex-col md:flex-row gap-9">
      <Imagesoon image="https://framerusercontent.com/images/hQVBeiDNGU2TfeDJALuhawlcto.jpg?scale-down-to=1024"
        word="BaselWorld" />
      <!-- <Videor video="https://framerusercontent.com/modules/assets/NieGBlxBdgpz9QCHV5Aj89rWjVg~DPEeC0jYyBwx9c865cOkUi-KzBM-3ukyhpgtPhvYo_U.mp4" 
      word="NYCB"
      /> -->
      <div class="max-w-[500px] max-h-[400px] flex-1 rounded-[20px] overflow-clip relative" @mouseenter="makeTrue"
        @mouseleave="makeFalse">
        <video class="pic_blur rounded-[20px] transition-all duration-300 scale-110 aspect-auto md:scale-y-150 sm:mt-10"
          :class="{ 'blur-md': Hovering, '': !Hovering }"
          src="https://framerusercontent.com/modules/assets/NieGBlxBdgpz9QCHV5Aj89rWjVg~DPEeC0jYyBwx9c865cOkUi-KzBM-3ukyhpgtPhvYo_U.mp4"
          alt="" autoplay loop @mouseover="hoverBlur" @mouseout="removeBlur"></video>
        <div
          class="text_in flex absolute transition-all duration-300 w-full justify-between items-center top-[5%] px-9 left-0 z-10 text-white"
          :class="{ 'opacity-0': !hoverEd, 'opacity-100': hoverEd }" @mouseenter="hoverBlur" @mouseleave="removeBlur">
          <p class="text-[20px] text-white">NYCB</p>
          <nuxt-link
            :to="'/about/?image=' + 'https://framerusercontent.com/modules/assets/NieGBlxBdgpz9QCHV5Aj89rWjVg~DPEeC0jYyBwx9c865cOkUi-KzBM-3ukyhpgtPhvYo_U.mp4' + '&name=' + 'NYCB'"
            class="material-icons text-[18px] bg-white text-black p-4 rounded-full hover:shadow-xl transition-all duration-[400ms]"
            :class="{ 'translate-y-[15px] translate-x-[-15px]': !hoverEd, 'translate]': hoverEd }">north_east</nuxt-link>
        </div>
      </div>
    </section>
    <LazyFooter v-motion :initial="InitialPos" :enter="EnterAnimation1" :delay="1300" />
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
    stiffness: 120,
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
    stiffness: 120,
    damping: 25,
    mass: 0.5,
  }
}


const hoverEd = ref(false);
const Hovering = ref(false)

const hoverBlur = () => {
  Hovering.value = true;
}

const removeBlur = () => {
  Hovering.value = false;
}

const { image, word } = defineProps(['image', 'word'])

const makeTrue = () => {
  hoverEd.value = true;
}

const makeFalse = () => {
  hoverEd.value = false;
}

</script>


