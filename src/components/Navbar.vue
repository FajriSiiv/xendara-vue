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

const navOpen = ref(false);

const OpenNav = () => {
  if (navOpen.value) {
    console.log("false");
    navOpen.value = false;
  } else {
    navOpen.value = true;
    console.log("true");
  }
};
</script>

<template>
  <nav class="h-[50px] px-20 flex justify-between mt-4 lg:px-5 z-10">
    <div class="flex justify-between gap-10 items-center text-primary">
      <span class="font-bold text-2xl flex">Xendara.io</span>

      <ul
        class="flex gap-7 items-end md:hidden"
        v-for="link in navLink"
        :key="link.name"
      >
        <li class="text-sm font-semibold">{{ link.name }}</li>
      </ul>
    </div>
    <div class="flex gap-3 items-center justify-center">
      <Button class="sm:hidden">Get started free</Button>
      <div class="ml-2 hidden md:block" @click="OpenNav">
        <v-icon name="io-menu" scale="2" />
      </div>
    </div>
  </nav>

  <ul
    :class="[
      ' flex flex-col justify-center items-center gap-y-6 bg-primary text-white w-full h-full transition-all left-0 top-0 fixed bottom-0 right-0 ',
      ,
      !navOpen ? '-translate-y-full' : 'translate-y-0',
    ]"
  >
    <li
      class="font-bold text-3xl hover:text-secondary transition-colors"
      v-for="(link, index) in navLink"
      :key="index"
    >
      {{ link.name }}
    </li>
    <div
      class="absolute right-10 top-10 text-white fill-white"
      @click="OpenNav"
    >
      <v-icon name="io-close" fill="#fff" scale="2" />
    </div>
  </ul>
</template>
