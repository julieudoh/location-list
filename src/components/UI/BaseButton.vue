<template>
  <button
    :type="type"
    :class="mode"
    class="bg-indigo-700 cursor-pointer py-3 px-6 border border-solid border-indigo-700 text-white hover:bg-indigo-800 active:bg-indigo-800 hover:border-indigo-800 active:border-indigo-800"
  >
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: ['type', 'mode'],
}
</script>

<style scoped>
.flat {
  background-color: transparent;
  color: #432dd7;
  border: none;
}
.flat:hover,
.flat:active {
  background-color: #a5b4fc;
}
</style>
