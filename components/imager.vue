<template>
  <div class="rounded-[20px] overflow-clip relative" @mouseenter="makeTrue(1)" @mouseleave="makeFalse(1)">
    <img class="pic_blur rounded-[20px] hover:blur-md transition-all duration-300"
      :class="{ 'blur-md': Hovering1, '': !Hovering1 }" :src="image" alt="">
    <div
      class="text_in flex absolute transition-all duration-300 w-full justify-between items-center top-[6%] px-8 left-0 z-10 text-white"
      :class="{ 'opacity-0': !hoverEd1, 'opacity-100': hoverEd1 }" @mouseenter="hoverBlur(1)" @mouseleave="removeBlur(1)">
      <p class="text-[20px] text-white">{{ word }}</p>
      <nuxt-link :to="'/about/?image=' + image + '&name=' + word"
        class="material-icons text-[18px] bg-white text-black p-3 rounded-full hover:shadow-xl transition-all duration-[400ms]"
        :class="{ 'translate-y-[15px] tran,,,,,slate-x-[-15px]': !hoverEd1, 'translate]': hoverEd1 }">north_east</nuxt-link>
    </div>
  </div>
</template>

<script setup>
const hoverEd1 = ref(false);
const hoverEd2 = ref(false);
const Hovering1 = ref(false)
const Hovering2 = ref(false)

const hoverBlur = (index) => {
  if (index === 1) {
    Hovering1.value = true;
  } else if (index === 2) {
    Hovering2.value = true;
  }
}

const removeBlur = (index) => {
  if (index === 1) {
    Hovering1.value = false;
  } else if (index === 2) {
    Hovering2.value = false;
  }
}

const { image, word } = defineProps(['image', 'word'])

const makeTrue = (index) => {
  if (index === 1) {
    hoverEd1.value = true;
  } else if (index === 2) {
    hoverEd2.value = true;
  }
}

const makeFalse = (index) => {
  if (index === 1) {
    hoverEd1.value = false;
  } else if (index === 2) {
    hoverEd2.value = false;
  }
}
</script>