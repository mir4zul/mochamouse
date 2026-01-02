<script setup>
import FavouriteImg from "@/assets/images/Favourite.png"
import Button from "@/components/Button.vue";
</script>

<template>
  <div class="from-accent/50 to-secondary/50 bg-gradient-to-b py-20">
    <div class="grid grid-cols-2 items-center max-w-7xl mx-auto">
      <img :src="FavouriteImg" alt="Favourite Image">
      <div class="max-w-lg mx-auto">
        <h2 class="font-inter text-primary text-6xl font-extrabold">Order Your Favourite Coffee</h2>
        <p class="font-inter text-popover mt-6 max-w-md text-xl font-thin">
          Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet
          sint. Velit officia consequat duis enim velit mollit. Exercitation
          veniam consequat sunt nostrud amet.
        </p>
        <Button class="mt-12" label="Order Now" variant="primary" size="md" />
      </div>
    </div>
  </div>
</template>

<style scoped></style>
