<template>
  <section class="p-[10px] sm:p-[30px] sm:px-[60px] flex flex-col md:flex-row gap-9">
    <div class="rounded-[20px] overflow-clip relative" @mouseenter="makeTrue(1)" @mouseleave="makeFalse(1)">
      <img class="pic_blur rounded-[20px] hover:blur-md transition-all duration-300"
        :class="{ 'blur-md': Hovering1, '': !Hovering1 }" :src="image1" alt="">
      <div
        class="text_in flex absolute transition-all duration-300 w-full justify-between items-center top-[6%] px-8 left-0 z-10 text-white"
        :class="{ 'opacity-0': !hoverEd1, 'opacity-100': hoverEd1 }" @mouseenter="hoverBlur(1)"
        @mouseleave="removeBlur(1)">
        <p class="text-[20px] text-white">{{ word1 }}</p>
        <nuxt-link :to="'/about/?image=' + image1 + '&name=' + word1"
          class="material-icons text-[18px] bg-white text-black p-3 rounded-full hover:shadow-xl transition-all duration-[400ms]"
          :class="{ 'translate-y-[15px] tran,,,,,slate-x-[-15px]': !hoverEd1, 'translate]': hoverEd1 }">north_east</nuxt-link>
      </div>
    </div>
    <div class="rounded-[20px] overflow-clip relative" @mouseenter="makeTrue(2)" @mouseleave="makeFalse(2)">
      <img class="pic_blur rounded-[20px] hover:blur-md transition-all duration-300"
        :class="{ 'blur-md': Hovering2, '': !Hovering2 }" :src="image2" alt="">
      <div
        class="text_in flex absolute transition-all duration-300 w-full justify-between items-center top-[6%] px-8 left-0 z-10 text-white"
        :class="{ 'opacity-0': !hoverEd2, 'opacity-100': hoverEd2 }" @mouseenter="hoverBlur(2)"
        @mouseleave="removeBlur(2)">
        <p class="text-[20px] text-white ">{{ word2 }}</p>
        <nuxt-link :to="'/about/?image=' + image2 + '&name=' + word2"
          class="material-icons text-[20px] bg-white text-black p-3 rounded-full transition-all duration-[400ms] hover:shadow-xl"
          :class="{ 'translate-y-[20px] translate-x-[-20px]': !hoverEd2, 'translate]': hoverEd2 }">north_east</nuxt-link>
      </div>
    </div>
  </section>
</template>

<script setup>
const hoverEd1 = ref(false);
const hoverEd2 = ref(false);
const Hovering1 = ref(false);
const Hovering2 = ref(false);

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

const { image1, image2, word1, word2 } = defineProps(['image1', 'image2', 'word1', 'word2'])

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

<style scoped></style>
