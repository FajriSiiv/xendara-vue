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
      'rounded-lg py-3 px-6 font-semibold w-fit',
      light
        ? 'bg-[#473BF0] bg-opacity-10 text-secondary'
        : 'bg-secondary text-white',
      transparent ? '!bg-transparent !text-secondary' : '',
    ]"
  >
    <slot></slot>
  </button>
</template>
