<template>
  <div class="flex-1 rounded-[20px] overflow-clip relative" @mouseenter="makeTrue(1)" @mouseleave="makeFalse">
    <video class="pic_blur rounded-[20px] transition-all duration-300 scale-110" :class="{ 'blur-md': Hovering, '': !Hovering }"
      :src="video" alt="" autoplay loop @mouseover="hoverBlur" @mouseout="removeBlur"></video>
    <div
      class="text_in flex absolute transition-all duration-300 w-full justify-between items-center top-[6%] px-8 left-0 z-10 text-white"
      :class="{ 'opacity-0': !hoverEd, 'opacity-100': hoverEd }" @mouseenter="hoverBlur" @mouseleave="removeBlur">
      <p class="text-[20px] text-white">{{ word }}</p>
      <nuxt-link :to="'/about/?image=' + video + '&name=' + word"
        class="material-icons text-[18px] bg-white text-black p-3 rounded-full hover:shadow-xl transition-all duration-[400ms]"
        :class="{ 'translate-y-[15px] tran,,,,,slate-x-[-15px]': !hoverEd, 'translate]': hoverEd }">north_east</nuxt-link>
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