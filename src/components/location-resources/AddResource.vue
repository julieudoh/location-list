<template>
  <base-card>
    <form @submit.prevent="submitData">
      <div class="my-4 mx-0">
        <label for="title" class="mb-2 block text-indigo-700 font-bold text-lg">Title</label>
        <input
          type="text"
          name="title"
          id="title"
          v-model="titleInput"
          class="block w-full p-[0.15rem] border border-solid border-[#ccc] focus:outline-none focus:border-indigo-700 focus:bg-indigo-200"
        />
      </div>
      <div class="my-4 mx-0">
        <label for="description" class="mb-2 block text-indigo-700 font-bold text-lg"
          >Description</label
        >
        <textarea
          type="text"
          name="description"
          id="description"
          rows="3"
          v-model="descriptionInput"
          class="block w-full p-[0.15rem] border border-solid border-[#ccc] focus:outline-none focus:border-indigo-700 focus:bg-indigo-200"
        ></textarea>
      </div>
      <div class="my-4 mx-0">
        <label for="link" class="mb-2 block text-indigo-700 font-bold text-lg">Link</label>
        <input
          type="text"
          name="link"
          id="link"
          v-model="linkInput"
          class="block w-full p-[0.15rem] border border-solid border-[#ccc] focus:outline-none focus:border-indigo-700 focus:bg-indigo-200"
        />
      </div>
      <div>
        <base-button type="submit">Add Resource</base-button>
      </div>
    </form>
  </base-card>
</template>

<script>
export default {
  inject: ['addResource'],
  data() {
    return {
      titleInput: '',
      descriptionInput: '',
      linkInput: '',
    }
  },
  methods: {
    submitData() {
      const enteredTitle = this.titleInput
      const enteredDescription = this.descriptionInput
      const enteredLink = this.linkInput

      console.log(enteredTitle, enteredDescription, enteredLink)
      this.addResource(enteredTitle, enteredDescription, enteredLink)
    },
  },
}
</script>
