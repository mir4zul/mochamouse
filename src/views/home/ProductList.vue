<script setup>
  import ExpressoDrink from "@/assets/images/Expresso_Homepage.jpg";
  import BeconBread from "@/assets/images/Bacon_Egg_Cheese_Croissant_Homepage.png";
  import HotCoffee from "@/assets/images/Hot_coffee_Homepage.jpg";
</script>

<template>
  <div class="grid grid-cols-4">
    <div class="group col-span-2 border-[0.5px] border-gray-300 pt-8">
      <div class="max-w-[500px] mx-auto text-center">
        <h2 class="text-gray-900 mb-1">Sipping is Believing</h2>
        <p class="text-primary font-dunkin text-2xl tracking-tight uppercase [word-spacing:-10px]">HAND CRAFTED ESPRESSO DRINKS</p>
      </div>
      <div class="flex justify-center">
        <img class="group-hover:scale-105 transition duration-300" :src="ExpressoDrink" alt="Expresso Drink">
      </div>
    </div>

    <div class="group border-[0.5px] border-gray-300 pt-8">
      <div class="max-w-[500px] mx-auto text-center">
        <h2 class="text-gray-900 mb-1" >Freshly Made</h2>
        <p class="text-primary font-dunkin text-2xl tracking-tight uppercase [word-spacing:-10px]" >ALL-DAY BREAKFAST SANDWICHES</p>
      </div>
     <div class="flex justify-center py-2">
        <img class="group-hover:scale-105 transition duration-300" :src="BeconBread" alt="Expresso Drink">
      </div>
    </div>

    <div class="group border-[0.5px] border-gray-300 pt-8">
      <div class="max-w-[500px] mx-auto text-center">
        <h2 class="text-gray-900 mb-1" >Dunkin’ Classic</h2>
        <p class="text-primary font-dunkin text-2xl tracking-tight uppercase [word-spacing:-10px]" >HOT COFFEE</p>
      </div>
      <div class="flex justify-center">
        <img class="group-hover:scale-105 transition duration-300" :src="HotCoffee" alt="Expresso Drink">
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>