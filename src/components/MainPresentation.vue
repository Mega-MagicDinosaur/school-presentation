<template>
  <div class="presentation-page">
    
    <div class="presentation-content">
      <swiper class="presentation-swiper"
        :slides-per-view="1"
        :space-between="0"
        @swiper="initSwiper"
        @slideChange="onSlideChange"
      >
        <swiper-slide class="swiper-slide"><presentation-slide title="First Slide" 
        :paragraphs="['first paragraph of slide number one', 'second paragraph of slide number one']"/>
        </swiper-slide>
        <swiper-slide class="swiper-slide"><presentation-slide title="Second Slide" 
        :paragraphs="['first paragraph of slide number two', 'second paragraph of slide number two']"/>
        </swiper-slide>
        <swiper-slide class="swiper-slide"><presentation-slide title="Third Slide" 
        :paragraphs="['first paragraph of slide number three', 'second paragraph of slide number three']"/>
        </swiper-slide>
      </swiper>
    </div>

  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';

import PresentationSlide from './PresentationSlide.vue';

export default defineComponent({
  name: 'MainPresentation',
  components: {
    Swiper,
    SwiperSlide,
    PresentationSlide
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