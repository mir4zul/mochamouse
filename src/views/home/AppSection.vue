<script setup>
  import backGroundImage from "@/assets/images/iphone_web.png";
  import AppStoreImage from "@/assets/images/AppStore.png";
  import GooglePlayImage from "@/assets/images/GooglePlayStore.png";

  const appSectionImageStyle = {
    backgroundImage: `url(${backGroundImage})`,
  };
</script>

<template>
  <div class="grid grid-cols-2">
    <div class="py-20 max-w-[600px] mx-auto">
      <div class="text-center">
        <p class="font-dunkin text-6xl tracking-wider font-bold text-secondary">DUNKIN<span
            class="text-primary">’</span></p>
        <p class="font-dunkin text-6xl [word-spacing:-25px]">DONE EASY</p>
      </div>
      <p class="text-gray-600 text-xl text-center py-8">Find a store, place your order and get on your way with the Dunkin’ App</p>

      <ul class="list-disc list-inside text-gray-600">
        <li>Order ahead and pay from your phone</li>
        <li>Join Dunkin’ Rewards and earn points towards free food and beverages</li>
        <li>Earn exclusive offers and rewards</li>
      </ul>

      <div class="flex gap-4 justify-center py-8">
        <button><img :src="AppStoreImage" alt="App Store icon"></button>
        <button><img :src="GooglePlayImage" alt="Google Play Store icon"></button>
      </div>
    </div>
    <div class="bg-center bg-no-repeat" :style="appSectionImageStyle"></div>

  </div>
</template>

<style scoped>

</style>