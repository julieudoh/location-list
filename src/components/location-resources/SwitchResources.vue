<template>
  <base-card>
    <base-button @click="switchResources('stored-resources')" :mode="storedRescourseButtonMode"
      >Stored Resources</base-button
    >
    <base-button @click="switchResources('add-resource')" :mode="addRescourseButtonMode"
      >Add Resource</base-button
    >
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
  provide() {
    return {
      resources: this.resources,
      addResource: this.addResource,
    }
  },
  computed: {
    storedRescourseButtonMode() {
      return this.selectedTab === 'stored-resources' ? null : 'flat'
    },
    addRescourseButtonMode() {
      return this.selectedTab === 'add-resource' ? null : 'flat'
    },
  },
  methods: {
    switchResources(tab) {
      this.selectedTab = tab
    },

    addResource(title, description, url) {
      const newResource = {
        id: new Date().toISOString(),
        title: title,
        description: description,
        link: url,
      }

      this.resources.unshift(newResource)
      this.selectedTab = 'stored-resources'
    },
  },
}
</script>
