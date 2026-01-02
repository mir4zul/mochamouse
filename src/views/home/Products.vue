<script setup>
  import ProductCard from "@/components/ProductCard.vue";
</script>

<template>
  <div class="from-secondary/50 to-secondary/75 bg-gradient-to-b h-screen py-20">
    <div class="mx-auto max-w-2xl">
      <h2 class="font-inter text-primary text-center text-6xl font-extrabold">Best Selling Coffee</h2>
      <p class="text-center max-w-lg mx-auto text-xl font-thin text-popover mt-4">
        A drink from the ‘My Alowishus’ bottled brews range OR
        grab one of our delicious coffee’s.
      </p>
    </div>
    <div class="max-w-7xl mx-auto grid grid-cols-3 gap-10 mt-52">
      <ProductCard v-for="product in 3" :key="product"/>
    </div>
  </div>
</template>

<style scoped></style>
