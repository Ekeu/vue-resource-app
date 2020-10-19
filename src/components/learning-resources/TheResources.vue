<template>
  <base-card>
    <base-button @click="setSectedTab('stored-resources')" :mode="storedResourceButtonMode">Stored Resources</base-button>
    <base-button @click="setSectedTab('add-resource')" :mode="addResourceButtonMode">Add Resource</base-button>
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
      storedResources: [
        {
          id: 'official-vue-guide',
          title: 'Official Vue Guide',
          description: 'The official Vue.js documentation',
          link: 'https://vuejs.org',
        },
        {
          id: 'official-react-guide',
          title: 'Official React Guide',
          description: 'The official React.js documentation',
          link: 'https://reactjs.org',
        },
        {
          id: 'google',
          title: 'Google',
          description: 'Learn how to google...',
          link: 'https://google.org',
        },
      ],
    };
  },
  provide() {
    return {
      resources: this.storedResources
    };
  },
  computed: {
    storedResourceButtonMode() {
      return this.selectedTab === 'stored-resources' ? null : 'flat'
    },
    addResourceButtonMode() {
      return this.selectedTab === 'add-resource' ? null : 'flat'
    }
  },
  methods: {
    setSectedTab(tab) {
        this.selectedTab = tab;
    } 
  }
};
</script>