
<template>
  <component :is="tag" v-bind="$attrs" :class="classes">
    <slot />
  </component>
</template>

<script setup>
import { computed } from 'vue';


const props = defineProps({
  tag: String,
  fontStyle: {
    type: String,
    required: false,
    default: 'h1',
    validator: (value) => ['h1', 'h2', 'h3', 'h4'].includes(value),
  },
  color: {
    type: String,
    required: false,
    default: 'text-brand-brown-500',
  }
});

const classes = computed(() => {
  const styleClasses = {
    h1: 'pb-2 text-5xl font-bold tracking-tighter font-heading leading-none',
    h2: 'pb-2 text-4xl font-bold tracking-tighter font-heading leading-none',
    h3: 'text-xl leading-none font-extralight',
    h4: 'pb-2 text-3xl font-bold tracking-tighter font-heading leading-none',
  }
  return ` ${styleClasses[props.fontStyle]} ${props.color}`;
});
</script>