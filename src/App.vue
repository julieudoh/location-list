<template>
  <the-header title="List of Fun Locations In Lagos"></the-header>
  <switch-resources></switch-resources>
</template>

<script>
import TheHeader from './components/layouts/TheHeader.vue'
import SwitchResources from './components/location-resources/SwitchResources.vue'

export default {
  components: {
    TheHeader,
    SwitchResources,
  },
}
</script>

<style scoped></style>
