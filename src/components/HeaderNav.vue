<script setup lang="ts">

</script>

<template>
  <ul class="nav">
    <li><a href="">Home</a></li>
    <li><div class="vertical-divider"></div></li>
    <li><a href="">Discounts</a></li>
    <li><div class="vertical-divider"></div></li>
    <li><a href="">About us</a></li>
  </ul>
</template>

<style scoped lang="postcss">
  .nav {
    @apply flex h-max gap-10
  }
  .vertical-divider {
    @apply bg-white h-full w-[1px]
  }
</style>