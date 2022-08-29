<template>
  <div class="presentation-page">
    
    <div class="presentation-content">
      
      <div class="swiper-button left" fill="clear">
        <ion-icon class="swiper-button-icon left" :class="(currentSlide == 0)? 'disabled' : ''"
        :icon="chevronDown" size="large" @click="onSwiperButtonClick(false)"/>
      </div>
      
      <swiper class="presentation-swiper"
        :slides-per-view="1"
        :space-between="0"
        @swiper="initSwiper"
        @slideChange="onSlideChange"
      >
        <swiper-slide v-for="(slide, index) in slidesData" :key="index" >
          <presentation-slide :title="slide.title" :paragraphs="slide.paragraphs" :images="slide.images"/>
        </swiper-slide>

      </swiper>
      
      <div class="swiper-button right" fill="clear">
        <ion-icon class="swiper-button-icon right" :class="(currentSlide == slidesData.length-1)? 'disabled' : ''"
        :icon="chevronDown" size="large" @click="onSwiperButtonClick(true)"/>
      </div>
    
    </div>

  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';

import { IonIcon, IonButton } from '@ionic/vue';
import { chevronDown } from 'ionicons/icons';

import PresentationSlide from './PresentationSlide.vue';

export default defineComponent({
  name: 'MainPresentation',
  components: {
    Swiper,
    SwiperSlide,
    PresentationSlide,
    IonIcon
  },
  setup() {
    const currentSlide = ref(0)
    const swiper = ref()
    const initSwiper = (swiperObj: any) => swiper.value = swiperObj
    const onSlideChange = () => currentSlide.value = swiper.value.activeIndex
    const onSwiperButtonClick = (direction: boolean) => {
      (direction == true)? swiper.value.slideNext() :
      swiper.value.slidePrev()
    }

    const slidesData = [
      {
        title: "First Slide",
        paragraphs: ['first paragraph of slide number one', 'second paragraph of slide number one'],
        images: []
      },
      {
        title: "Second Slide",
        paragraphs: ['first paragraph of slide number two', 'second paragraph of slide number two'],
        images: []
      },
      {
        title: "Third Slide",
        paragraphs: ['first paragraph of slide number three', 'second paragraph of slide number three'],
        images: []
      },
      {
        title: "Third Slide",
        paragraphs: ['first paragraph of slide number three', 'second paragraph of slide number three'],
        images: []
      },
      {
        title: "Third Slide",
        paragraphs: ['first paragraph of slide number three', 'second paragraph of slide number three'],
        images: []
      },
      {
        title: "Third Slide",
        paragraphs: ['first paragraph of slide number three', 'second paragraph of slide number three'],
        images: []
      },
      {
        title: "Third Slide",
        paragraphs: ['first paragraph of slide number three', 'second paragraph of slide number three'],
        images: []
      }
    ]

    return {
      initSwiper,
      onSlideChange,
      onSwiperButtonClick,

      currentSlide,
      slidesData,

      // icons
      chevronDown,
    }
  },
});
</script>

<style scoped lang="scss" src="../assets/style/MainPresentationStyle.scss"></style>