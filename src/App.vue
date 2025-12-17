<template>
  <the-header title="List of Fun Locations In Lagos"></the-header>
  <stored-resources :resources="resources"></stored-resources>
</template>

<script>
import TheHeader from './components/layouts/TheHeader.vue'
import StoredResources from './components/location-resources/StoredResources.vue'

export default {
  components: {
    TheHeader,
    StoredResources,
  },
  data() {
    return {
      resources: [
        {
          id: '001',
          title: 'Ikeja City Mall',
          description: 'A lively place to go with friends and family',
          link: 'https://www.ikejacitymall.com.ng/',
        },
        {
          id: '002',
          title: 'Landmark Beach',
          description: 'A lively place to go with friends and family',
          link: 'https://landmarkhotel.ng/',
        },
        {
          id: '003',
          title: 'Lekki Conservative Center',
          description: 'A lively place to go with friends and family',
          link: 'https://ncfnigeria.org/lekki-conservation-centre-the-green-soul-of-lagos-metropolis/',
        },
      ],
    }
  },
}
</script>

<style scoped></style>
