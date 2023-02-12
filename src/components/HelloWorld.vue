<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <p>
      You’ve successfully created a project with
      <a href="https://vitejs.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
    </p>
  </div>
</template>

<style scoped>
h1 {
  font-weight: 500;
  font-size: 1.8rem;
  top: -10px;
}

.greetings h1 {
  text-align: left;
}
</style>
