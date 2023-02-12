<script setup>
import HelloWorld from "../components/HelloWorld.vue";
import { useCounterStore } from "@/stores/counter";
import { ipcRenderer } from "electron";

ipcRenderer.on("main-process-message", (_event, ...args) => {
  console.log("[Receive Main Process Message]:", ...args);
});
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
