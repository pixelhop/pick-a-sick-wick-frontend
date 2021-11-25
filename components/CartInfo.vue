<template>
  <button class="flex items-center snipcart-checkout">
    <span class="pr-2 ml-3 text-lg font-semibold text-brand-grey-800 snipcart-total-price">£24</span>
    <Cart class="w-6" />
  </button>
</template>
<script>

import Cart from './icons/cart.vue'

export default defineComponent({
  components: {
    Cart
  }
})
</script>
<style scoped>
.router-link-active {
  @apply text-brand-orange;
}
</style>