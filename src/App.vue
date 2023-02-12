<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <header>
    <div class="wrapper">
      <img alt="Logo" class="logo" src="@/assets/logo.svg" />
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/nodejs">Node.js</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
    </div>
  </header>
  <RouterView />
</template>

<style scoped>
.wrapper {
  display: flex;
  padding: 10px;
  align-items: center;
}

.logo {
  width: 35px;
  height: 35px;
}

nav {
  text-align: center;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
}
</style>
