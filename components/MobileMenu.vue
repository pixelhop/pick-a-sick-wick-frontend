<template>
  <nav class="fixed inset-0 z-50 flex items-center justify-center bg-brand-beige-300">
    <button
      class="absolute p-1 right-4 top-8 text-brand-grey-800"
      title="Close"
      @click="$emit('close')"
    >
      <svg
        xmlns="http://www.w3.org/2000/svg"
        class="w-6 h-6"
        fill="none"
        viewBox="0 0 24 24"
        stroke="currentColor"
      >
        <path
          stroke-linecap="round"
          stroke-linejoin="round"
          stroke-width="2"
          d="M6 18L18 6M6 6l12 12"
        />
      </svg>
    </button>
    <NavBar />
  </nav>
</template>

<script setup>
const route = useRoute();
const emit = defineEmits(['close'])

watch(route, () => {
  emit('close');
});
</script>

<style>
</style>
