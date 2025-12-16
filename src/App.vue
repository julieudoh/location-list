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
// import TheHeader from './components/layouts/TheHeader.vue'
import LocationResource from './components/location-resources/LocationResource.vue'

export default {
  components: {
    // TheHeader,
    LocationResource,
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
  methods: {
    storedResources() {
      console.log(this.resources.length)
    },
  },
}
</script>

<style scoped></style>
