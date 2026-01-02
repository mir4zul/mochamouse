<script setup>
  import HeroImg from "@/assets/images/imgHero_Desktop@2x.png";
  import DunkinRewardsLogo from "@/assets/images/Dunkin' Rewards Logo - Text_Desktop.svg";
  import Button from "@/components/Button.vue";

  const heroSectionImageStyle = {
    backgroundImage: `url(${HeroImg})`,
  };
</script>

<template>
  <div
      class="bg-center bg-cover bg-no-repeat pt-20 pb-28"
      :style="heroSectionImageStyle"
  >
    <div class="max-w-3xl mx-auto">
      <div>
        <img :src="DunkinRewardsLogo" class="mx-auto" alt="">
      </div>
      <div class="text-center leading-16 mt-6">
        <h1 class="font-dunkin font-bold text-[3.5rem] text-gray-700 ">MAKE THE MOST</h1>
        <h1 class="font-dunkin font-bold text-[3.5rem] text-gray-700">OF YOUR DUNKIN’ RUN!</h1>
      </div>
      <div class="text-center max-w-xl text-gray-700 text-base mx-auto mt-4">
        <p class="pb-6">
          Calling all Dunkin’ fans! Join Dunkin’ Rewards today to enjoy
          exclusive offers and start earning points toward
          FREE food and drinks. The more you visit, the more benefits you unlock!
        </p>
        <Button label="Join Now" variant="primary" size="lg" />
      </div>
    </div>
  </div>
</template>
