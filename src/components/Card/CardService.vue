<script setup>
import Button from "../Button.vue";

const props = defineProps({
  imgUrl: {
    type: String,
    default: "",
  },
  description: {
    type: String,
    default: "",
  },
  nameService: {
    type: String,
    default: "Web Development",
  },
  background: {
    type: String,
    default: "bg-secondary",
  },
});
</script>

<template>
  <div
    :class="[
      'p-3  text-white flex flex-col gap-3 rounded-md text-center w-fit md:w-full ',
      background,
    ]"
  >
    <div class="h-full py-10 mx-auto">
      <img v-bind:src="[imgUrl]" :alt="[nameService]" />
    </div>
    <span class="font-semibold text-xl">{{ nameService }}</span>
    <p class="max-w-[300px] text-sm mx-auto">
      {{ description }}
    </p>
    <Button class="!text-white !bg-transparent mx-auto mt-5">Learn more</Button>
  </div>
</template>
