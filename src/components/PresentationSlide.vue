<template>
  <div class="slide-container">
    <span>{{ title }}</span> <br>

    <span v-for="(paragraph, index) in paragraphs" :key="index">
      {{ paragraph }} <br>
    </span>

  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
    
export default defineComponent({
  name: 'PresentationSlide',
  components: {},
  setup(props) {

    return {
    }
  },
  props: {
    title: {
      type: String,
      required: true
    },
    paragraphs: {
      type: Array<string>,
      required: true
    },
    images: {
      type: Array<string>,
      required: false
    }
  }
});
</script>

<style scoped lang="scss" src="../assets/style/PresentationSlideStyle.scss"></style>