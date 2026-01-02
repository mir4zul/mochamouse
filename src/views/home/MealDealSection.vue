<script setup>
  import backgroundImageUrl from "@/assets/images/img_Home_Desktop@2x.png"
  import Button from "@/components/Button.vue";
</script>

<template>
  <div class="grid grid-cols-2 bg-center bg-cover bg-no-repeat"  :style="{ backgroundImage: `url(${backgroundImageUrl})` }">
    <div class="py-14">
      <div class="flex items-center pl-14 my-6">
        <p class="text-primary font-dunkin text-[14rem] leading-7">
          $6
        </p>
        <div class="">
          <p class="text-secondary text-8xl font-dunkin">Meal</p>
          <p class="text-secondary text-8xl font-dunkin">Deal</p>
        </div>
      </div>
      <div class="px-6">
        <div class="flex justify-center">
          <Button label="View Menu" variant="primary" size="lg" />
        </div>
        <p class="text-center text-sm mt-4 text-gray-700">
          No substitutions. Participation may vary.
          Limited time offer. Cannot be combined with
          other offers. Exclusions and terms apply.
        </p>
      </div>
    </div>
    <div></div>
  </div>
</template>

<style scoped>

</style>