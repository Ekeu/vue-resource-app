<template>
  <base-card>
    <base-button @click="setSectedTab('stored-resources')">Stored Resources</base-button>
    <base-button @click="setSectedTab('add-resource')">Add Resource</base-button>
  </base-card>
  <component :is="selectedTab"></component>
</template>

<script>
import StoredResources from './StoredResources.vue';
import AddResource from './AddResource.vue'

export default {
  components: {
    StoredResources,
    AddResource
  },
  data() {
    return {
      selectedTab: 'stored-resources',
    };
  },
  methods: {
    setSectedTab(tab) {
        this.selectedTab = tab;
    } 
  }
};
</script>