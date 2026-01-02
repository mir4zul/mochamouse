<script setup>
import CategoryCard from "@/components/CategoryCard.vue";
</script>

<template>
  <div class="from-primary-foreground/50 to-accent/50 bg-gradient-to-b py-20">
    <div class="mx-auto max-w-2xl">
      <h2 class="font-inter text-primary text-center text-6xl font-extrabold">
        Explore Our Alowishus
      </h2>
      <p
        class="font-inter text-popover mx-auto mt-4 max-w-xl px-4 text-center text-xl font-thin"
      >
        A drink from the ‘My Alowishus’ bottled brews range OR grab one of our
        delicious coffee’s.
      </p>
    </div>
    <div class="mx-auto mt-20 grid max-w-7xl grid-cols-3 gap-10">
      <CategoryCard v-for="i in 3" :key="i" />
    </div>
  </div>
</template>

<style scoped></style>
