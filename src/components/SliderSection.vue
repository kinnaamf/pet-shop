<script setup lang="ts">
import SliderContainer from "@/components/SliderContainer.vue";

const title = "The best discounts"
</script>

<template>
  <div class="slider-section">
    <h2 class="title">{{ title }}</h2>
    <SliderContainer/>
  </div>
</template>

<style scoped lang="postcss">
.slider-section {
  @apply text-white flex flex-col justify-center items-center pt-24
}

</style>
<style lang="postcss">
.title {
  @apply uppercase font-semibold text-[70px];
}
</style>