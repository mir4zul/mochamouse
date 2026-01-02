<script setup>
  import Mocha from '@/assets/images/Mocha.png'
  import Button from '@/components/Button.vue'
</script>

<template>
  <div class="bg-primary-foreground shadow-xl shadow-secondary/35 hover:shadow-secondary/50 transition-all duration-200 flex flex-col justify-between items-center rounded-3xl py-10 px-8">
    <div class="">
      <h3 class="font-inter font-bold text-4xl text-primary">Our Catering</h3>
      <p class="font-inter font-thin text-popover pt-4">Alowishus Catering, delicious drop off Catering</p>
    </div>
    <img class="w-80" :src="Mocha" alt="">
    <Button class="mt-4" label="Order Now" variant="secondary" size="md" />
  </div>
</template>

<style scoped></style>
