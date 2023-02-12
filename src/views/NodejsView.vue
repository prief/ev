<script setup>
import { ref } from "vue";
import { userInfo } from "node:os";
let username = userInfo().username;
let user = ref(username);
</script>
<template>
  <div class="nodejs">
    <p>Node.js got your computer's user is "{{ user }}"</p>
  </div>
</template>

<style></style>
