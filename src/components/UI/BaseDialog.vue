<template>
  <teleport to="body">
    <div
      @click="$emit('close')"
      class="fixed top-0 left-0 h-screen w-full bg-[rgba(0,0,0,0.75)] z-10"
    ></div>
    <dialog
      open
      class="fixed top-[20vh] left-[10%] w-[80%] z-100 rounded-xl border-none shadow-[0_2px_8px_rgba(0,0,0,0.26)] p-0 my-0 mx-auto overflow-hidden md:left-[calc(50% - 20rem)] md:w-160"
    >
      <header class="bg-indigo-700 text-white w-full p-4 text-xl">
        <slot name="header">
          <h2 class="m-0">{{ title }}</h2>
        </slot>
      </header>
      <section class="p-4">
        <slot></slot>
      </section>
      <menu class="p-4 flex justify-end m-0">
        <slot name="actions"> </slot>
      </menu>
    </dialog>
  </teleport>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: false,
    },
  },
  emits: ['close'],
}
</script>
