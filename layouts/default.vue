<template>
  <div class="relative font-body">
    <HeaderSection />
    <div class="pt-24 bg-brand-beige-300">
      <slot />
    </div>
    <subscribe />
    <FooterSection />
  </div>
</template>



<style scoped>
body {
  -webkit-font-smoothing: antialiased;
}
</style>