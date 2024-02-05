<template>
  <div  class="max-w-[500px] max-h-[400px] flex-1 rounded-[20px] overflow-clip relative cursor-pointer" @click="navigateTo(`/about/?image=${image}&name=${word}`)" @mouseenter="makeTrue"
    @mouseleave="makeFalse">
    <video class="pic_blur rounded-[20px] transition-all duration-300 scale-110 aspect-auto md:scale-125"
      :class="{ 'blur-md': Hovering, '': !Hovering }" :src="video" alt="" autoplay loop @mouseover="hoverBlur"
      @mouseout="removeBlur"></video>
    <div
      class="text_in flex absolute transition-all duration-300 w-full justify-between items-center top-[5%] px-9 left-0 z-10 text-white"
      :class="{ 'opacity-0': !hoverEd, 'opacity-100': hoverEd }" @mouseenter="hoverBlur" @mouseleave="removeBlur">
      <p class="text-[20px] text-white">{{ word }}</p>
      <nuxt-link :to="'/about/?image=' + video + '&name=' + word"
        class="material-icons text-[18px] bg-white text-black p-4 rounded-full hover:shadow-xl transition-all duration-[400ms]"
        :class="{ 'translate-y-[15px] translate-x-[-15px]': !hoverEd, 'translate]': hoverEd }">north_east</nuxt-link>
    </div>
  </div>
</template>

<script setup>
const hoverEd = ref(false);
const Hovering = ref(false)

const hoverBlur = () => {
  Hovering.value = true;
}

const removeBlur = () => {
  Hovering.value = false;
}

const { video, word } = defineProps(['video', 'word'])

const makeTrue = () => {
  hoverEd.value = true;
}

const makeFalse = () => {
  hoverEd.value = false;
}
</script>