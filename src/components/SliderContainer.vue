<script setup lang="ts">
import { ref, computed } from "vue";
import slide1 from "@/assets/images/slide1.jpg";
import slide2 from "@/assets/images/slide2.jpg";
import slide3 from "@/assets/images/slide3.jpg";
import slide4 from "@/assets/images/slide4.jpg";
import slide5 from "@/assets/images/slide5.jpg";
import slide6 from "@/assets/images/slide6.jpg";
import slide7 from "@/assets/images/slide7.jpg";
import slide8 from "@/assets/images/slide8.jpg";
import slide9 from "@/assets/images/slide9.jpg";
import ArrowIcon from "@/components/icons/ArrowIcon.vue";

const sliderImages = [
  slide1, slide2, slide3, slide4, slide5,
  slide6, slide7, slide8, slide9,
];

const currentIndex = ref(0);

const visibleSlides = computed(() => {
  const len = sliderImages.length;
  return [
    sliderImages[(currentIndex.value - 1 + len) % len],
    sliderImages[currentIndex.value],
    sliderImages[(currentIndex.value + 1) % len],
  ];
});

const prev = () => {
  currentIndex.value = (currentIndex.value - 1 + sliderImages.length) % sliderImages.length;
};

const next = () => {
  currentIndex.value = (currentIndex.value + 1) % sliderImages.length;
};

const setSlide = (index: number) => {
  currentIndex.value = index;
};
</script>

<template>
  <div class="slider-wrapper">
    <div class="slider-container relative">
      <ArrowIcon class="slider-arrow left-0" @click="prev" />

      <div
          v-for="(image, index) in visibleSlides"
          :key="index"
          class="slider-item"
          :class="index === 1 ? 'w-9/12 h-screen' : 'w-2/12 opacity-60'"
          :style="{ backgroundImage: `url(${image})` }"
      ></div>

      <ArrowIcon class="slider-arrow right-0 rotate-180" @click="next" />
    </div>

    <!-- Dots -->
    <div class="dots-container">
      <button
          v-for="(image, index) in sliderImages"
          :key="index"
          class="dot-button"
          :class="index === currentIndex ? 'bg-[#BC7E2D]' : 'bg-amber-100'"
          @click="setSlide(index)"
      ></button>
    </div>
  </div>
</template>

<style scoped lang="postcss">
.slider-wrapper {
  @apply px-[256px] mt-8 w-full h-[700px];
}

.slider-container {
  @apply h-full w-full flex items-center gap-4 justify-between relative;
}

.slider-item {
  @apply h-4/6 bg-center bg-cover rounded-xl transition-all duration-500 shadow-md;
}
.slider-item:nth-child(3) {
  @apply h-5/6 shadow-2xl;
}
.slider-arrow {
  @apply absolute top-1/2 -translate-y-1/2 cursor-pointer z-20 ;
}

.dots-container {
  @apply flex gap-4 justify-center;
}

.dot-button {
  @apply w-3 h-3 rounded-full bg-white transition-colors duration-300;
}
</style>
