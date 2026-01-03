<script setup>
import { ref } from "vue";
import { ArrowRightIcon, ArrowLeftIcon } from "@heroicons/vue/16/solid";
import ReviewCard from "@/components/ReviewCard.vue";

const TOTAL_CARDS = 10;
const VISIBLE_CARDS = 4;
const CARD_WIDTH = 320;
const LEFT_PEEK = CARD_WIDTH / 3;

const currentIndex = ref(0);
const maxIndex = TOTAL_CARDS - VISIBLE_CARDS;

const next = () => {
  if (currentIndex.value < maxIndex) currentIndex.value++;
};

const prev = () => {
  if (currentIndex.value > 0) currentIndex.value--;
};
</script>

<template>
  <div class="from-secondary to-primary/75 bg-gradient-to-b py-20">
    <div class="grid grid-cols-7 gap-10">
      <!-- SLIDER -->
      <div class="relative col-span-4 overflow-hidden">
        <div
          class="flex gap-6 transition-transform duration-500 ease-in-out"
          :style="{
            transform: `translateX(-${currentIndex * CARD_WIDTH + LEFT_PEEK}px)`,
          }"
        >
          <ReviewCard v-for="i in TOTAL_CARDS" :key="i" class="min-w-[320px]" />
        </div>
      </div>

      <!-- CONTENT -->
      <div class="col-span-3">
        <div class="max-w-md">
          <h2 class="font-inter text-primary text-6xl font-extrabold">
            What Our Customers Say
          </h2>

          <div class="flex items-center gap-6 pt-10">
            <p class="font-inter text-popover text-4xl font-extrabold">4.9</p>
            <div>
              <div class="flex gap-1">
                <StarIcon
                  v-for="i in 5"
                  :key="i"
                  class="h-6 w-6 text-yellow-400"
                />
              </div>
              <p class="font-inter text-popover pt-2">based on 2452+ reviews</p>
            </div>
          </div>

          <!-- ARROWS -->
          <div class="flex items-center gap-6 pt-10">
            <button
              @click="prev"
              :disabled="currentIndex === 0"
              class="disabled:opacity-40"
            >
              <ArrowLeftIcon
                class="text-popover bg-accent h-10 w-10 rounded-full p-2"
              />
            </button>

            <button
              @click="next"
              :disabled="currentIndex === maxIndex"
              class="disabled:opacity-40"
            >
              <ArrowRightIcon
                class="text-popover bg-accent h-10 w-10 rounded-full p-2"
              />
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
