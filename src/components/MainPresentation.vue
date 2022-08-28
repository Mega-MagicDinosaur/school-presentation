<template>
  <div class="presentation-page">
    
    <div class="presentation-content">
      <swiper class="presentation-swiper"
        :slides-per-view="1"
        :space-between="0"
        @swiper="initSwiper"
        @slideChange="onSlideChange"
      >
        <swiper-slide class="swiper-slide">Slide 1</swiper-slide>
        <swiper-slide class="swiper-slide">Slide 2</swiper-slide>
        <swiper-slide class="swiper-slide">Slide 3</swiper-slide>
      </swiper>
    </div>

  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';

export default defineComponent({
  name: 'MainPresentation',
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    const currentSlide = ref(0)
    const swiper = ref()
    const initSwiper = (swiperObj: any) => swiper.value = swiperObj
    const onSlideChange = () => currentSlide.value = swiper.value.activeIndex 
    return {
      initSwiper,
      onSlideChange
    }
  }
});
</script>

<style scoped lang="scss" src="../assets/style/MainPresentationStyle.scss"></style>