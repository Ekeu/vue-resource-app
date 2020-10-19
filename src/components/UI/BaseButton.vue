<template>
  <button :type="type" :class="mode">
    <slot></slot>
  </button>
</template>

<script>
export default {
  props: ['type', 'mode'],
};
</script>

<style scoped>
button {
  padding: 0.75rem 1.5rem;
  font-family: inherit;
  background-color: #6F2232;
  border: 1px solid #6F2232;
  color: white;
  cursor: pointer;
}

button:hover,
button:active {
  background-color: #501924;
  border-color: #501924;
}

.flat {
  background-color: transparent;
  color: #6F2232;
  border: none;
}

.flat:hover,
.flat:active {
  background-color: #dadae4;
}
</style>