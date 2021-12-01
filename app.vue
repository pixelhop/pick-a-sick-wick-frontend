<template>
  <Title>Pick a Sick Wick - Candle Shop</Title>
  <NuxtPage />
</template>

<style>
body {
  @apply text-brand-grey bg-brand-beige-300;
}
</style>

<script setup>
const router = useRouter();

// Scroll to top after each navigation
router.afterEach(() => {
  window.scrollTo(0, 0);
});
</script>