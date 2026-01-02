<script setup>
  import Button from "@/components/Button.vue";
  import Product from "@/assets/images/drip-coffee-single.png";
</script>

<template>
  <div class="bg-primary-foreground shadow-xl shadow-secondary/35 hover:shadow-secondary/50 transition-all duration-200 items-center rounded-3xl py-10 px-8">
    <div class="grid grid-cols-2">
      <img class="-mt-32" :src="Product" alt="Product Image">
      <div>
        <p class="text-secondary/50 text-sm font-thin">#1 Selling</p>
        <h3 class="font-inter font-bold text-4xl text-primary pt-2">Double Espresso</h3>
      </div>
    </div>
    <p class="text-popover font-thin pt-10 pb-12">
      Amet minim mollit non deserunt dolor ullamco est sit aliqua
      dolor do amet sint. Velit officia consequat duis.
    </p>
    <div class="flex items-center justify-between">
      <p class="text-primary font-inter font-bold text-2xl">$59.99</p>
      <Button label="Order Now" variant="secondary" size="md" />
    </div>
  </div>
</template>

<style scoped></style>
