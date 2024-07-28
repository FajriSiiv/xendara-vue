<script setup>
defineProps({
  light: {
    type: Boolean,
    default: false,
  },
  arrow: {
    type: Boolean,
    default: false,
  },
  transparent: {
    type: Boolean,
    default: false,
  },
});
</script>

<template>
  <button
    :class="[
      'rounded-lg py-3 px-6 font-semibold w-fit h-fit',
      light
        ? 'bg-[#473BF0] bg-opacity-10 text-secondary'
        : 'bg-secondary text-white',
      transparent ? '!bg-transparent !text-secondary' : '',
    ]"
  >
    <slot></slot>

    <span class="ml-5" v-if="arrow">
      <v-icon name="fa-arrow-right" />
    </span>
  </button>
</template>
