<script setup lang="ts">

import LogoIcon from "@/components/icons/LogoIcon.vue";
import HeaderNav from "@/components/HeaderNav.vue";
import AuthStatus from "@/components/AuthStatus.vue";
</script>

<template>
  <header class="header">
    <LogoIcon/>
    <HeaderNav/>
    <AuthStatus/>
  </header>
</template>

<style scoped lang="postcss">
.header {
  @apply flex justify-between py-4 px-24 bg-[#191919] text-white text-[28px] font-medium z-10 relative;
}
</style>