<template>
  <stored-resources :resources="storedResources"></stored-resources>
</template>

<script>
import StoredResources from './components/learning-resources/StoredResources.vue';

export default {
  components: {
    StoredResources,
  },
  data() {
    return {
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
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=B612:wght@400;700&display=swap');

* {
  box-sizing: border-box;
}

html {
  font-family: 'B612', 'sans-serif';
}

body {
  margin: 0;
}
</style>