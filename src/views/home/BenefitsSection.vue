<script setup>
  import EarningsImg from "@/assets/images/Earn_Points_tab.png";
  import GetRewardsImg from "@/assets/images/Get_rewards_tab.png";
  import EarnMoreImg from "@/assets/images/Boosted_status_tab.png";
  import Button from "@/components/Button.vue";

  const benefits = [
    {
      title: "EARN POINTS ANY WAY YOU PAY",
      description: "Order ahead in the app or scan your Dunkin' Rewards ID in-store to earn 10 points per $1 spent.",
      img: EarningsImg
    },
    {
      title: "GET REWARDS AND OFFERS",
      description: "Enjoy exclusive offers and redeem rewards starting at just 150 points — only $15 spent!",
      img: GetRewardsImg
    },
    {
      title: "UNLOCK MORE WITH BOOSTED STATUS",
      description: "Earn faster when you visit 12 times in a calendar month and start receiving 12 points per $1 spent!",
      img: EarnMoreImg
    }
  ]
</script>

<template>
  <div class="max-w-5xl grid grid-cols-3 gap-10 mx-auto">
    <div
        v-for="(item, index) in benefits"
        :key="index"
        class="py-10"
    >
      <img
          class="w-[200px] mx-auto"
          :src="item.img"
          :alt="item.title"
      />

      <h2
          class="font-dunkin pt-2 pb-4 text-[22px] font-light [word-spacing:-8px] text-center max-w-[250px] mx-auto"
      >
        {{ item.title }}
      </h2>

      <p
          class="text-center text-gray-700 text-base font-medium leading-5 max-w-[280px] mx-auto"
      >
        {{ item.description }}
      </p>
    </div>
  </div>

  <div class="flex justify-center items-center pb-10">
    <Button label="Learn More" variant="primary" size="lg"/>
  </div>
</template>


<style scoped>

</style>