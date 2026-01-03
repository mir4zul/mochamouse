<script setup>
  import logo from "@/assets/images/Logo.png";
  import email from "@/assets/images/email.svg";
  import phone from "@/assets/images/phone.svg";
  import facebook from "@/assets/images/facebook.svg";
  import twitter from "@/assets/images/twitter.svg";
  import instagram from "@/assets/images/instagram.svg";
  import linkedin from "@/assets/images/linkedin.svg";
  import Button from "@/components/Button.vue";
</script>

<template>
  <div class="from-primary/75 to-primary bg-gradient-to-b py-10">
    <div class="mx-auto max-w-7xl">
      <div class="grid grid-cols-3">
        <div class="col-span-2">
          <div class="max-w-lg">
            <img class="w-32" :src="logo" alt="logo">
            <p class="text-primary-foreground/80 text-xl mt-6">
              We made it our mission to create community everyday
              and grow meaningful, lasting relationships with our
              staff, our suppliers and of course you, our customers.
            </p>
          </div>
          <div class="mt-12">
            <h4 class="text-3xl font-bold text-primary-foreground tracking-wider">Store Locations</h4>
            <p class="text-primary-foreground/80 text-xl mt-4 max-w-md">
              Find your nearest Alowishus store with opening hours,
              location and contact details.
            </p>
          </div>
        </div>

        <div class="col-span-1">
          <div class="flex flex-col gap-6">
            <h4 class="text-3xl font-bold text-primary-foreground tracking-wider">Contact Alowishus!</h4>
            <div class="flex gap-2 items-center">
              <div class="bg-white p-2 rounded-full">
                <img :src="email" alt="">
              </div>
              <p class="text-primary-foreground/80 text-xl">alowishus@gmai.com</p>
            </div>
            <div class="flex gap-2 items-center">
              <div class="bg-white p-2 rounded-full">
                <img :src="phone" class="w-7" alt="">
              </div>
              <p class="text-primary-foreground/80 text-xl">+110 214 214 2451</p>
            </div>
            <div class="flex gap-4">
              <div class="bg-white p-2 rounded-full">
                <img :src="facebook" class="w-7" alt="facebook">
              </div>
              <div class="bg-white p-2 rounded-full">
                <img :src="instagram" class="w-7" alt="instagram">
              </div>
              <div class="bg-white p-2 rounded-full">
                <img :src="twitter" class="w-7" alt="twitter">
              </div>
              <div class="bg-white p-2 rounded-full">
                <img :src="linkedin" class="w-7" alt="linkedin">
              </div>
            </div>
          </div>
          <div class="space-y-4 mt-10">
            <h4 class="text-3xl font-bold text-primary-foreground tracking-wider">First One’s On Us!</h4>
            <input class="w-full p-3 rounded-full border border-primary-foreground/20 bg-primary-foreground/20 px-6" placeholder="Enter your email" type="text">
          </div>
          <div>
            <Button class="mt-10" label="Subscribe" variant="secondary" size="lg" />
          </div>
        </div>
      </div>
      <div class="flex justify-between pt-12 border-t border-primary-foreground/20 mt-12">
        <p>
          <span class="text-primary-foreground/60">Copytright © 2022</span> <strong class="text-primary-foreground">Alowishus Delicious</strong>
        </p>
        <p class="flex gap-4 text-primary-foreground/60">
          <span>Terms of Use</span>
          <span>|</span>
          <span>Privacy Policy</span>
        </p>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
