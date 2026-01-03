<script setup>
  import { StarIcon } from "@heroicons/vue/24/solid";
  import Image from "@/assets/images/manImage.jpg";
</script>

<template>
  <div class="rounded-2xl bg-gradient-to-br from-secondary to-primary/25">
    <img :src="Image" class="w-full h-60 object-cover rounded-t-2xl" alt="" />

    <div class="mt-4 p-6">
      <div class="flex items-center gap-2">
        <p class="font-semibold text-white">Imam White</p>

        <StarIcon
          v-for="i in 5"
          :key="i"
          class="h-5 w-5 text-yellow-400"
        />
      </div>

      <p class="mt-2 text-white/80 text-sm">
        “Amet minim mollit non deserunt ullamco est sit
        aliqua dolor do amet sint. Velit officia consequat
        duis enim velit mollit. Exercitation veniam consequat
        sunt nostrud amet. Amet minim mollit non deserunt
        ullamco est sit aliqua dolor do amet sint.
        Velit officia”
      </p>
    </div>
  </div>
</template>

<style scoped></style>
