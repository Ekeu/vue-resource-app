<template>
  <the-header title="Resource App"></the-header>
  <the-resources></the-resources>
</template>

<script>
import TheHeader from './components/layouts/TheHeader.vue'
import TheResources from './components/learning-resources/TheResources.vue'

export default {
  components: {
    TheHeader,
    TheResources
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