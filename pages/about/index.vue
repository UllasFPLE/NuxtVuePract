<template>
  <div class="w-full flex justify-center items-center flex-col mt-16">
    <section class="max-w-[1200px] p-[40px] h-[500px] flex justify-center items-center flex-col gap-8">
      <h1 class="text-[36px] md:text-[48px] xl:text-[72px] text-center font-medium">{{ Heading }}</h1>
      <p class="text-[14px] px-[12px] py-[8px] bg-[#e8e5e480] rounded-3xl text-black text-nowrap">{{ name }}</p>
    </section>
  </div>
</template>

<script setup>
const name = ref('')
const imageParam = ref('')
const Heading = ref('')

onMounted(() => {
  // Assuming your URL is something like: http://example.com/page?image=imageValue
  const queryString = window.location.search;
  const params = new URLSearchParams(queryString);

  // Accessing the 'image' parameter
  imageParam.value = params.get('image');
  name.value = params.get('name');

  if (name.value === 'Ari') {
    Heading.value = 'A better way to deal with every day'
  }
  if (name.value === 'Correlated') {
    Heading.value = 'From onboarding to automation.\nA seamless user journey.';
  }
  if (name.value === 'Ari') {
    Heading.value = 'A better way to deal with every day'
  }
  if (name.value === 'Ari') {
    Heading.value = 'A better way to deal with every day'
  }
  if (name.value === 'Ari') {
    Heading.value = 'A better way to deal with every day'
  }
  if (name.value === 'Ari') {
    Heading.value = 'A better way to deal with every day'
  }
});


definePageMeta({
  layout: "service"
})
</script>