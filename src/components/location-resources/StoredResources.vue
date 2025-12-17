<template>
  <ul>
    <location-resource
      v-for="res in resources"
      :key="res.id"
      :id="res.id"
      :title="res.title"
      :description="res.description"
      :link="res.link"
    ></location-resource>
  </ul>
</template>

<script>
import LocationResource from './LocationResource.vue'

export default {
  props: ['resources'],
  components: {
    LocationResource,
  },
}
</script>
