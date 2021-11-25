<template>
  <button v-bind="$attrs" :class="classes">
    <slot />
  </button>
</template>

<script setup>
import { computed } from 'vue';

const props = defineProps({
  theme: {
    type: String,
    required: false,
    default: 'primary',
    validator: (value) => ['primary', 'secondary'].includes(value),
  },
});

const classes = computed(() => {
  const themeClasses = {
    'primary': 'px-6 py-4 text-2xl font-bold text-white shadow-xl bg-brand-orange font-heading rounded-none',
    'secondary': 'px-6 py-4 text-2xl font-bold text-brand-orange border border-3 border-brand-orange font-heading rounded-none',
  }
  return themeClasses[props.theme];
});

</script>

