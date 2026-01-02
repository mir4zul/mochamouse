<script setup>
  import BackGroundImage from "@/assets/images/Google_map_web.png"
  import Button from "@/components/Button.vue"

  const googleLocationSectionImageStyle = {
    backgroundImage: `url(${BackGroundImage})`,
  };
</script>

<template>
  <div class="h-[600px] grid grid-cols-5">
    <div class="bg-cover bg-center bg-no-repeat col-span-3" :style="googleLocationSectionImageStyle" ></div>
    <div class="col-span-2 text-center pt-16">
      <h1 class="text-6xl font-bold uppercase text-gray-800 tracking-wider font-dunkin [word-spacing:-30px]">Come Visit</h1>
      <p class="text-gray-800 text-2xl pt-4">Find a Dunkin' Near You</p>

      <Button class="mt-10" label="Find a Location" variant="primary" size="lg" />
    </div>
  </div>
</template>

<style scoped>

</style>