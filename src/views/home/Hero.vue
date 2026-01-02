<script setup>
  import Button from "@/components/Button.vue";
  import ChocoBallDonut from "@/assets/images/CHOCOBALL_DONUT.png";
  import { StarIcon } from "@heroicons/vue/24/solid";
</script>

<template>
  <div class="max-w-[1440px] mx-auto">
  <div
      class="grid grid-cols-2 justify-center items-center py-10"
  >
    <div>
      <h1 class="font-inter text-9xl font-extrabold text-primary">Mochamuse Coffee & Donut</h1>
      <p class="font-inter text-popover max-w-sm py-10">A drink from the ‘My Alowishus’ bottled brews range OR grab one of our delicious coffee’s.</p>
      <Button label="Order Now" variant="primary" size="lg" />
    </div>
    <div class="w-[715px] relative">
      <img class="-rotate-[22deg]" :src="ChocoBallDonut" alt="">
      <div class="absolute bg-accent top-7/12 left-14 p-6 rounded-3xl max-w-[250px] text-sm">
        <div class="flex gap-1">
          <StarIcon
            v-for="i in 5"
            :key="i"
            class="h-6 w-6 text-primary"
          />
        </div>

        <p class="text-popover font-normal pt-2">4.9 out of 5 Overall Star Rating for All Local Business.</p>
      </div>
    </div>
  </div>
  </div>
</template>
