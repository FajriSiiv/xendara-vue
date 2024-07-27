<script setup>
import { ref } from "vue";
import Button from "./Button.vue";

const navLink = ref([
  {
    name: "Demos",
    url: "/demos",
  },
  {
    name: "Pages",
    url: "/pages",
  },
  {
    name: "Support",
    url: "/support",
  },
  {
    name: "Contact",
    url: "/contact",
  },
]);
</script>

<template>
  <nav class="h-[50px] px-20 flex justify-between mt-4">
    <div class="flex justify-between gap-10 items-center text-primary">
      <span class="font-bold text-2xl flex">Xendara.io</span>

      <ul class="flex gap-7 items-end" v-for="link in navLink" :key="link.name">
        <li class="text-sm font-semibold">{{ link.name }}</li>
      </ul>
    </div>
    <Button>Get started free</Button>
  </nav>
</template>
