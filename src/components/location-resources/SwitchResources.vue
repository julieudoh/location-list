<template>
  <base-card>
    <base-button @click="switchResources('stored-resources')" :resources="resources"
      >Stored Resources</base-button
    >
    <base-button @click="switchResources('add-resource')">Add Resource</base-button>
  </base-card>
  <keep-alive>
    <component :is="selectedTab"></component>
  </keep-alive>
</template>

<script>
import StoredResources from './StoredResources.vue'
import AddResource from './AddResource.vue'

export default {
  components: {
    StoredResources,
    AddResource,
  },
  data() {
    return {
      selectedTab: 'stored-resources',
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
    switchResources(tab) {
      this.selectedTab = tab
      console.log(this.selectedTab)
    },
  },
}
</script>
