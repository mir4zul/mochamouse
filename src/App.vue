<script setup>
import { ref } from "vue";
import Button from "@/components/Button.vue";
import DunkinSvg from "@/assets/images/dd_nav_logo.svg";
import Location from "@/assets/images/Locate.svg";

const isOpen = ref(false);
</script>

<template>
  <div class="max-w-[1480px] mx-auto bg-white">
    <!--  Desktop view for Navigation  -->
    <div class="sticky top-0 z-50 bg-white xl:block hidden">
      <header class="flex justify-end font-montserrat p-3 border-b border-gray-300">
        <div class="flex gap-4">
          <button class="font-bold text-xs uppercase tracking-wider border-2 border-gray-900 px-10 py-1 rounded-full">Careers</button>
          <button class="font-extrabold text-xs uppercase tracking-wider border-2 border-gray-900 px-2 py-1 rounded-full">Join Rewards</button>
          <Button label="Sign In" variant="primary" size="sm" />
        </div>
      </header>

      <nav class="nav text-gray-700 font-medium flex justify-between items-center uppercase text-base">
        <router-link to="/" class="nav-link font-dunkin">Menu</router-link>
        <router-link to="/contact" class="nav-link font-dunkin">Locations</router-link>
        <router-link to="/delivery" class="nav-link font-dunkin">Delivery</router-link>
        <router-link to="/delivery" class="font-dunkin font-bold text-3xl tracking-wider text-secondary">Dunkin'</router-link>
        <router-link to="/dunkin-rewards" class="nav-link font-dunkin">Dunkin Rewards</router-link>
        <router-link to="/dunkin-card" class="nav-link font-dunkin">Dunkin Card</router-link>
        <router-link to="/shop" class="nav-link font-dunkin">Shop</router-link>
        <!--      <router-link to="/careers" class="nav-link font-dunkin">Careers</router-link>   -->
      </nav>
    </div>

    <!-- Mobile view -->
    <div class="xl:hidden">
      <!-- Header (always visible) -->
      <header class="fixed top-0 left-0 right-0 z-50 bg-white border-b">
        <div class="flex items-center justify-between px-4 py-8">
          <!-- Menu Button (always visible) -->
          <button
            class="hamburger"
            :class="{ open: isOpen }"
            @click="isOpen = !isOpen"
            aria-label="Menu"
          >
            <span></span>
            <span></span>
            <span></span>
          </button>

          <!-- Logo -->
          <router-link to="/" class="font-dunkin text-3xl">
            <img :src="DunkinSvg" alt="dunkin logo" />
          </router-link>

          <!-- Location -->
          <img :src="Location" alt="location" />
        </div>

        <nav
          v-show="!isOpen"
          class="flex justify-around items-center p-4 transition-opacity duration-200"
        >
          <router-link to="/" class="font-dunkin">Menu</router-link>
          <router-link to="/delivery" class="font-dunkin">Delivery</router-link>
          <router-link to="/dunkin-rewards" class="font-dunkin">Dunkin Rewards</router-link>
        </nav>
      </header>

      <!-- Overlay -->
      <div
        v-show="isOpen"
        class="fixed inset-0 bg-black/40 z-40"
        @click="isOpen = false"
      ></div>

      <!-- Top to Bottom Menu -->
      <nav
        class="fixed top-10 left-0 right-0 bg-white z-40
           min-h-screen pt-24 px-6
           transform transition-transform duration-300 ease-in-out"
        :class="isOpen ? 'translate-y-0' : '-translate-y-full'"
      >
        <div class="flex gap-4 justify-center">
          <Button label="Sign In" variant="primary" size="lg" />
          <Button label="Join Rewards" variant="primary" size="lg" />
        </div>
        <div class="flex flex-col gap-6">
          <router-link @click="isOpen = false" to="/" class="nav-link font-dunkin">Menu</router-link>
          <router-link @click="isOpen = false" to="/contact" class="nav-link font-dunkin">Locations</router-link>
          <router-link @click="isOpen = false" to="/delivery" class="nav-link font-dunkin">Delivery</router-link>
          <router-link @click="isOpen = false" to="/dunkin-rewards" class="nav-link font-dunkin">Dunkin Rewards</router-link>
          <router-link @click="isOpen = false" to="/dunkin-card" class="nav-link font-dunkin">Dunkin Card</router-link>
          <router-link @click="isOpen = false" to="/shop" class="nav-link font-dunkin">Shop</router-link>
        </div>
      </nav>

      <!-- Push content down because header is fixed -->
      <div class="pt-24"></div>
    </div>

    <!--  Content Area  -->
    <router-view />
  </div>
</template>


<style scoped>
.nav {
  display: flex;
  gap: 1.5rem;
  padding: 1rem;
}

.nav-link {
  position: relative;
  display: inline-block;
  text-decoration: none;
  transition: color 0.3s ease;
}

/* underline */
.nav-link::after {
  content: "";
  position: absolute;
  left: 0;
  bottom: -4px;
  width: 100%;
  height: 2px;
  background-color: #ec4899; /* pink underline */
  transform: scaleX(0);
  transform-origin: center; /* animate from center */
  transition: transform 250ms ease-in-out;
}

/* hover: text color pink + underline animation */
.nav-link:hover {
  color: #ec4899; /* pink text */
}

.nav-link:hover::after {
  transform: scaleX(1);
}

/* active route: text-gray-900 + underline pink */
.router-link-active {
  color: #ec4899; /* text-gray-900 */
}

.router-link-active::after {
  transform: scaleX(1);
}


/* Hamburger menu */
.hamburger {
  width: 28px;
  height: 22px;
  position: relative;
  cursor: pointer;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.hamburger span {
  display: block;
  height: 3px;
  width: 100%;
  background-color: #1f2937; /* gray-800 */
  border-radius: 2px;
  transition: all 0.3s ease;
}

/* OPEN STATE → 2 bars (X) */
.hamburger.open span:nth-child(1) {
  transform: translateY(9px) rotate(45deg);
}

.hamburger.open span:nth-child(2) {
  opacity: 0;
}

.hamburger.open span:nth-child(3) {
  transform: translateY(-9px) rotate(-45deg);
}

</style>