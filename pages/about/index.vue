<template>
  <div>
    about {{ name }}
  </div>
</template>

<script setup>
const name = ref('')

onMounted(() => {
  // Assuming your URL is something like: http://example.com/page?image=imageValue
  const queryString = window.location.search;
  const params = new URLSearchParams(queryString);

  // Accessing the 'image' parameter
  const imageParam = params.get('image');
  name.value = params.get('name');
});

</script>