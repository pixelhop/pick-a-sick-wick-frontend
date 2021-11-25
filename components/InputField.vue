<template>
  <input
    class="w-24 px-4 py-4 text-xl bg-black rounded-none outline-none bg-opacity-10 placeholder-brand-grey-600 text-brand-grey-600"
    :placeholder="placeholder"
    :type="type"
    :value="modelValue"
    @change="$emit('update:modelValue', $event.target.value)"
    name="text"
  />
</template>


<script setup>
const props = defineProps({
  type: String,
  placeholder: String,
  modelValue: [String, Number]
});
</script>

<style scoped>
</style>