<script setup>

import BackGroundImage from "@/assets/images/img_2023-Holiday_desktop@2x.png";
import Button from "@/components/Button.vue";

const holidaySectionImageStyle = {
  backgroundImage: `url(${BackGroundImage})`,
};
</script>

<template>
  <div class="bg-cover bg-center bg-no-repeat" :style="holidaySectionImageStyle">
    <div class="max-w-2xl mx-auto py-16">
      <h1 class="text-5xl pt-10 uppercase leading-16 mx-auto text-center font-bold font-dunkin text-primary tracking-wider">UNWRAP HOLIDAY CHEER</h1>
      <p class="max-w-[400px] mx-auto text-center text-primary py-10">The perfect pick-me-up for everyone on your list. Give the gift of Dunkin’ this holiday season!</p>
      <div class="flex justify-center">
        <Button label="Shop Holiday" variant="primary" size="lg" />
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>