<template>
  <div class="footer-page">
    
    <div class="footer-content" :fullscreen="true">
      <span>Made With</span> <br>

      <img class="icon-image" src="../assets/media/ionic_logo.png" alt="ionic">
      <img class="icon-image" src="../assets/media/vue_logo.png" alt="vue">

      <span>Minor Contributions & Other Technologies</span> <br>

      <img class="icon-image" src="../assets/media/html_css_js_logo.png" alt="HTML/css/js">
      <img class="icon-image" src="../assets/media/sass_logo.png" alt="sass">
      <img class="icon-image" src="../assets/media/typescript_logo.png" alt="type script">
      <img class="icon-image" src="../assets/media/swiper_logo.png" alt="swiper">

      <br>

      <img class="icon-image" src="../assets/media/git_logo.png" alt="git">
      <img class="icon-image" src="../assets/media/eslint_logo.png" alt="eslint">
      <img class="icon-image" src="../assets/media/npm_logo.png" alt="npm">
      
      <br>

      <img class="icon-image" src="../assets/media/jest_logo.png" alt="jest">
      <img class="icon-image" src="../assets/media/cypress_logo.png" alt="cypress">

    </div>

  </div>
</template>

<script lang="ts">
import { IonContent, IonPage } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'MainFooter',
  components: {}
});
</script>

<style scoped lang="scss" src="../assets/style/MainFooterStyle.scss"></style>