<template>
  <base-card>
    <li>
      <header class="flex justify-between">
        <h2 class="text-lg font-bold">{{ title }}</h2>
        <button>Delete</button>
      </header>
      <p class="text-base">{{ description }}</p>
      <nav class="pt-2">
        <a :href="link" class="text-blue-500">View Location</a>
      </nav>
    </li>
  </base-card>
</template>

<script>
export default {
  props: ['id', 'title', 'description', 'link'],
}
</script>
