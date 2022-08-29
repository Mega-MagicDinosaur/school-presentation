<template>
  <div class="footer-page">
    
    <div class="footer-content" :fullscreen="true">

      <ion-grid class="footer-grid">

        <ion-row class="grid-row"><ion-col class="grid-col title-col">Frameworks</ion-col></ion-row>

        <ion-row class="grid-row"> <!-- main -->
          <ion-col class="grid-col"><footer-card name="ionic" image="ionic_logo.png" link="" class="footer-icon" /></ion-col>
          <ion-col class="grid-col"><footer-card name="vue" image="vue_logo.png" link="" class="footer-icon"/></ion-col>
        </ion-row>

        <ion-row class="grid-row"><ion-col class="grid-col title-col">Libraries/Languages</ion-col></ion-row>

        <ion-row class="grid-row"> <!-- other libraries -->
          <ion-col class="grid-col"><footer-card name="swiper" image="swiper_logo.png" link="" class="footer-icon"/></ion-col>
          <ion-col class="grid-col"><footer-card name="sass" image="sass_logo.png" link="" class="footer-icon"/></ion-col>
          <ion-col class="grid-col"><footer-card name="type script" image="typescript_logo.png" link="" class="footer-icon"/></ion-col>
        </ion-row>

        <ion-row class="grid-row"><ion-col class="grid-col title-col">Useful Tools</ion-col></ion-row>

        <ion-row class="grid-row"> <!-- tools -->
          <ion-col class="grid-col"><footer-card name="git" image="git_logo.png" link="" class="footer-icon"/></ion-col>
          <ion-col class="grid-col"><footer-card name="eslint" image="eslint_logo.png" link="" class="footer-icon"/></ion-col>
          <ion-col class="grid-col"><footer-card name="npm" image="npm_logo.png" link="" class="footer-icon"/></ion-col>
        </ion-row>

        <ion-row class="grid-row"><ion-col class="grid-col title-col">E2E/Unit Testing</ion-col></ion-row>

        <ion-row class="grid-row"> <!-- testing -->
          <ion-col class="grid-col"><footer-card name="jest" image="jest_logo.png" link="" class="footer-icon"/></ion-col>
          <ion-col class="grid-col"><footer-card name="cypress" image="cypress_logo.png" link="" class="footer-icon"/></ion-col>
        </ion-row>

      </ion-grid>

    </div>

  </div>
</template>

<script lang="ts">
import { IonGrid, IonRow, IonCol } from '@ionic/vue';
import { defineComponent } from 'vue';

import FooterCard from './FooterCard.vue';

export default defineComponent({
  name: 'MainFooter',
  components: {
    FooterCard,
    IonGrid, 
    IonRow, 
    IonCol
  }
});
</script>

<style scoped lang="scss" src="../assets/style/MainFooterStyle.scss"></style>