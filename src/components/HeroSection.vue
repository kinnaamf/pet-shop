<script setup lang="ts">
  import background from "@/assets/images/background.jpg"
  import HeroContent from "@/components/HeroContent.vue";
</script>

<template>
  <div
      class="hero-wrapper"
      :style="{ backgroundImage: `url(${background})` }"
  >
  <div class="hero-overlay"></div>
    <div class="hero-content">
        <HeroContent/>
    </div>
  </div>
</template>

<style scoped lang="postcss">
.hero-wrapper {
  @apply relative w-full z-0 bg-cover bg-center h-screen text-white;
}
.hero-overlay {
  @apply absolute inset-0 bg-[#D17B0F]/40 -z-10;
}
.hero-content {
  @apply relative z-10 h-full flex flex-col gap-8 justify-center;
}
</style>