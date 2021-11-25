<template>
  <div>
    <section class="relative mb-20 -mt-24 border-b-4 md:mb-10 header border-brand-beige">
      <div class="absolute inset-0 z-0 overflow-hidden">
        <img :src="HeaderBg" class="object-cover w-full h-full" alt="Pick a sick wick" />
      </div>

      <div class="relative z-20 h-full header-content">
        <div class="absolute flex flex-col justify-center p-8 mx-auto hero-box">
          <div class="px-6 py-8 bg-white rounded-lg drop-shadow-2xl">
            <heading tag="h3" font-style="h3">Smelly candles</heading>
            <heading tag="h2" font-style="h2">Only the sickest wicks</heading>
            <p class="pb-4 pr-4 text-brand-gray font-body">
              If you’re like us and can’t get enough of burning
              things in your own home, pick a sick wick and
              <span
                class="font-bold"
              >feed your burning habbit safely with added benifit of smelling delicious.</span>
            </p>
            <btn class="absolute md:-right-3 md:-bottom-3">Shop Now</btn>
          </div>
        </div>
      </div>
    </section>

    <section class="mb-28">
      <Container>
        <div class="w-full mx-auto mb-12 text-center md:w-2/3 lg:w-1/3">
          <heading tag="h2" font-style="h3">Our Candles</heading>
          <heading tag="h3" font-style="h2" class="mb-2">Show me the sick wicks</heading>
          <p>All our candles our hand made and 100% verified to satisfy any pyromaniac’s itch to burn things in a safe way.</p>
        </div>

        <div class="grid grid-cols-2 gap-12 md:grid-cols-4">
          <product-teaser
            class="col-span-1"
            v-for="product in products.data"
            :key="product.id"
            :product="product"
          />
        </div>

        <div class="flex justify-center mt-10">
          <btn theme="secondary">View all the sick wicks</btn>
        </div>
      </Container>
    </section>
  </div>
</template>

<script setup>
import HeaderBg from 'assets/images/header-bg.jpg';
const config = useRuntimeConfig();
const { data: products } = await useFetch(`${config.API_URL}/api/products?pagination[start]=0&pagination[limit]=4&populate=*`)
</script>

<style scoped>
.header {
  height: 600px;
  /* margin-top: -106px;   */
}

@screen md {
  .hero-box {
    left: 10%;
    top: 175px;
    width: 485px;
  }
}
@screen md {
  .header {
    height: 700px;
  }
}

@screen md {
  .home-head-image {
    top: -110px;
    height: 770px;
    width: 100%;
  }
}

.hero-box {
  bottom: -50px;
  left: 0px;
  width: 100%;
}

@screen md {
  .hero-box {
    left: 10%;
    top: 100px;
    width: 485px;
  }
}
</style>
