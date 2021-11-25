<template>
  <div>
    <Container class="grid grid-cols-12 gap-2 pt-32 pb-24 md:gap-12">
      <div class="col-span-12 md:col-span-6 lg:col-span-5">
        <ProductImage :product="product.data" />
      </div>
      <div class="col-span-12 md:col-span-6 lg:col-span-7">
        <heading tag="h2" font-style="h1">{{ product.data.attributes.Title }}</heading>
        <p class="mb-6 text-2xl text-brand-grey-600">£{{ product.data.attributes.Price }}</p>
        <p class="pr-12 mb-6 text-brand-grey-400">{{ product.data.attributes.Description }}</p>

        <div class="flex items-center">
          <input-field type="number" class="mr-4" />
          <btn>Add to basket</btn>
        </div>
      </div>
    </Container>
    <Container>
      <div class="pb-8">
        <heading tag="h3" font-style="h3">Related products</heading>
        <heading tag="h2" font-style="h2">Other sick wicks</heading>
      </div>
      <div class="grid grid-cols-2 gap-12 md:grid-cols-4">
        <product-teaser
          class="col-span-1"
          v-for="product in products.data"
          :key="product.id"
          :product="product"
        />
      </div>
      <div class="flex justify-center pt-12 pb-32">
        <btn theme="secondary">View the other sick wicks</btn>
      </div>
    </Container>
  </div>
</template>

<script setup>
const route = useRoute();
const config = useRuntimeConfig();
const { data: products } = await useFetch(`${config.API_URL}/api/products?populate=*`)
const { data: product } = await useFetch(`${config.API_URL}/api/products/${route.params.id}?populate=*`)
</script>

<style scoped>
.product-image {
  width: 545px;
}
</style>