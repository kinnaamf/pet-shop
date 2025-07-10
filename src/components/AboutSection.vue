<script setup lang="ts">
import image1 from "@/assets/images/card1.jpg"
import image2 from "@/assets/images/card2.jpg"
import image3 from "@/assets/images/card3.jpg"
import image4 from "@/assets/images/card4.jpg"
import image5 from "@/assets/images/card5.jpg"
import AboutCard from "@/components/AboutCard.vue";
const title = 'about us'
</script>

<template>
  <div class="about-container">
    <h1 class="title text-center">{{ title }}</h1>
  </div>
  <AboutCard/>
</template>

<style scoped lang="postcss">
  .about-container {
    @apply mt-12
  }
  .cards-container {
    @apply w-full h-[70vh] px-40 mt-12 grid grid-cols-3 gap-4 mb-12
  }
  .card {
    @apply bg-center bg-cover bg-no-repeat rounded-2xl relative
  }

</style>