<script setup>
import Button from "@/components/Button.vue";
import Image1 from "@/assets/images/mochaBanner_1.jpg";
import Image2 from "@/assets/images/mochaBanner_2.jpg";
</script>

<template>
  <div
    class="from-secondary/75 to-secondary bg-gradient-to-b py-20"
  >
    <!-- Content -->
    <div class="relative z-10 h-[675px] max-w-6xl mx-auto grid grid-cols-2">
      <!-- Left -->
      <div class="flex flex-col justify-center">
        <h2 class="font-inter text-primary text-6xl font-extrabold">
          Instant Coffee At Your Home
        </h2>

        <p class="font-inter text-popover mt-6 max-w-md text-xl font-thin">
          Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet
          sint. Velit officia consequat duis enim velit mollit.
        </p>

        <div>
          <Button class="mt-12" label="Order Now" variant="primary" size="md" />
        </div>
      </div>

      <!-- Right Images -->
      <div class="relative">
        <img
          :src="Image1"
          class="w-60 border-8 right-24 h-[675px] -rotate-12 absolute object-cover rounded-2xl shadow-xl top-0"
          alt=""
        />
        <img
          :src="Image2"
          class="w-60 border-8 right-0 h-[675px] absolute object-cover rounded-2xl shadow-xl"
          alt=""
        />
      </div>
    </div>
  </div>
</template>
