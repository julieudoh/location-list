<template>
  <header class="w-full h-20 flex items-center justify-center bg-indigo-600">
    <h1 class="text-xl text-white m-0">{{ title }}</h1>
  </header>
</template>

<script>
export default {
  props: ['title'],
}
</script>
