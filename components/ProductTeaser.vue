<template>
  <article>
    <nuxt-link :to="`/products/${product.id}`" class="group">
      <ProductImage
        :product="product"
        class="mb-6 transition-transform transform shadow-xl group-hover:scale-105"
      />
      <Heading tag="h3" font-style="h4">{{ product.attributes.Title }}</Heading>
      <p class="text-lg text-brand-grey-400">£{{ product.attributes.Price }}</p>
    </nuxt-link>
  </article>
</template>

<script setup>
const props = defineProps({
  product: Object
});
</script>
