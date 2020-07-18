<template>
  <h1 class="header">{{ msg }}</h1>
  <button
    class="btn btn-blue"
    @click="count++"
  >
    count is: {{ count }}
  </button>
  <p>Edit <code>components/HelloWorld.vue</code> to test hot module replacement.</p>
</template>

<script setup>
import { ref, computed } from 'vue'

export default {
  props: { msg: String }
}

export const count = ref(0)
export const color = 'red';
</script>

<style vars="{ color }" scoped>
.header {
  @apply text-3xl font-bold;
  color: var(--color);
}
.btn {
  @apply font-bold py-2 px-4 rounded;
}
.btn-blue {
  @apply bg-blue-500 text-white;
}
.btn-blue:hover {
  @apply bg-blue-700;
}
</style>
