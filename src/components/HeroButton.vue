<script setup lang="ts">
const buttonText = "Get started"
</script>

<template>
  <button class="hero-button">
    {{ buttonText }}
  </button>
</template>

<style scoped lang="postcss">
.hero-button {
  @apply bg-[#D17B0F] py-6 px-10 rounded-full font-bold text-[27px] w-max
}
</style>