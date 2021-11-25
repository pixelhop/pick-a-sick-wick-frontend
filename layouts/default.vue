<template>
  <div class="relative font-body">
    <HeaderSection />
    <div class="pt-24 bg-brand-beige-300">
      <slot />
      <div
        hidden
        id="snipcart"
        data-api-key="Y2I4NzBlMzMtZGQ1Yi00N2UzLWEyN2UtNjYwYjk2OTZlYWM4NjM3NjkyMTAxMzI2ODkyNjgy"
      ></div>
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