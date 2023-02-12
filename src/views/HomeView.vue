<script setup>
import HelloWorld from "../components/HelloWorld.vue";
import { useCounterStore } from "@/stores/counter";
const counter = useCounterStore();
</script>

<template>
  <main>
    <HelloWorld msg="Hi." />
    <p>
      You've clicked {{ counter.count }} times.
      <button @click="counter.increment()">click</button>
    </p>
  </main>
</template>
