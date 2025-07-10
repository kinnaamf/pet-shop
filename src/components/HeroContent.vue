<script setup lang="ts">
import HeroButton from "@/components/HeroButton.vue";

const title = "LET’S MAKE \n" +
    "YOUR PET\n" +
    "HAPPIER!"
const subtitle = "The Best Products For Your Favourite\nMember Of The Family."
</script>

<template>
  <div class="hero-content">
    <h1 class="title">{{ title }}</h1>
    <div class="horizontal-line"></div>
    <h3 class="subtitle">{{ subtitle }}</h3>

    <HeroButton/>
  </div>
</template>

<style scoped lang="postcss">
.hero-content {
  @apply text-white flex flex-col justify-center h-full items-center gap-5 self-end relative right-[200px];
}


.horizontal-line {
  @apply bg-[#D17B0F] h-[3px] w-full
}


</style>

<style lang="postcss">
.subtitle {
  @apply whitespace-pre-line text-[24px] font-medium text-white
}

.title {
  @apply whitespace-pre-line font-black text-[80px] text-white uppercase leading-tight;
}
</style>