<template>
  <div class="relative flex justify-center w-full h-64 pb-16 mt-14 subscribe-bg">
    <Container>
      <div class="w-full mx-auto lg:w-3/6">
        <div class="px-10 -mt-12 text-center bg-white rounded-lg shadow-xl py-9 subscribe-box">
          <Heading tag="h3" font-style="h3">Subscribe</heading>
          <Heading tag="h2" font-style="h2">Never miss a wick</heading>
          <p
            class="w-full px-2 mx-auto text-center pb-7 text-brand-grey-400"
          >Subscribe to receice the worlds most cutting edge candle news direct to your inbox. Our newsletter is on fire.</p>
          <div class="flex items-center">
            <input-field type="email" placeholder="Your email" class="w-3/4 mr-8" />
            <btn class="h-full">Subscribe</btn>
          </div>
        </div>
      </div>
    </Container>
  </div>
</template>


<style>
.subscribe-bg {
  background: url("assets/images/subscribe-pattern.png") repeat, #e9ba9e;
}
</style>