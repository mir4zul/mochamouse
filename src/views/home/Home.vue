<script setup>
import Hero from "@/views/home/Hero.vue";
import Category from "@/views/home/Category.vue";
import Favourite from "@/views/home/Favourite.vue";
import Products from "@/views/home/Products.vue";
import MealDealSection from "@/views/home/MealDealSection.vue";
import AppSection from "@/views/home/AppSection.vue";
import ProductList from "@/views/home/ProductList.vue";
import Holiday from "@/views/home/Holiday.vue";
import GoogleLocation from "@/views/home/GoogleLocation.vue";

</script>

<template>
  <!--  Hero Section -->
  <Hero/>

<!--  &lt;!&ndash; Benefits Section &ndash;&gt;-->
<!--  <BenefitsSection />-->

  <!-- Category Section -->
  <Category />

  <!-- Favourite Section -->
  <Favourite />

  <!-- Products Section -->
  <Products />

  <!--  MealDealSection -->
  <MealDealSection/>

  <!-- AppSection -->
  <AppSection/>

  <!-- ProductList -->
  <ProductList/>

  <!-- Holiday -->
  <Holiday/>

  <!-- GoogleLocation -->
  <GoogleLocation/>
</template>

<style scoped>

</style>