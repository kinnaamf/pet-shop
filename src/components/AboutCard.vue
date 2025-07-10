<script setup lang="ts">
import image1 from "@/assets/images/card1.jpg";
import image2 from "@/assets/images/card2.jpg";
import image3 from "@/assets/images/card3.jpg";
import image4 from "@/assets/images/card4.jpg";
import image5 from "@/assets/images/card5.jpg";

const firstContent = [
  {
    title: '<span class="font-normal">Discover</span>\n' + 'Dogs',
    image: image1,
  },
  {
    title: '<span class="font-normal">Explore</span>\n' + 'Rats',
    image: image2,
  },
  {
    title: '<span class="font-normal">View</span>\n' + 'All Products',
    image: image3,
  },
]
const secondContent = [
  {
    title: '<span class="font-normal">Discover</span>\n' + 'Cats',
    image: image4,
  },
  {
    title: '<span class="font-normal">Our</span>\n' + 'Friends',
    image: image5,
  },
]
</script>

<template>
  <!--  <div class="dark-overlay"></div>-->
  <div class="card-container">
    <div class="card-section ">
      <div
          class="card first"
          v-for="(content, index) in firstContent"
          :key="index"
          :style="{backgroundImage: 'url(' + content.image + ')'}"
      >
        <div class="card-content ">
          <span v-html="content.title"></span>
        </div>
        <div class="dark-overlay"></div>
      </div>
    </div>
    <div class="card-section">
      <div
          class="card second"
          v-for="(content, index) in secondContent"
          :key="index"
          :style="{backgroundImage: 'url(' + content.image + ')'}"
      >
        <div class="card-content">
          <span v-html="content.title"></span>
        </div>
        <div class="dark-overlay"></div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="postcss">
.card-container {
  @apply h-[80vh] flex flex-col px-40 mt-12 gap-6 mb-12
}

.card-section {
  @apply h-[500px] flex gap-6
}

.card-content {
  @apply text-white text-[64px] font-medium whitespace-pre-line;
}

.first {
  @apply flex items-center justify-center
}

.card {
  @apply w-full h-full bg-center bg-no-repeat bg-cover rounded-2xl relative -z-20
}
.second {
  @apply flex items-end pl-8 pb-4
}
.dark-overlay {
  @apply absolute inset-0 bg-[#333]/30 rounded-2xl -z-10;
}
</style>