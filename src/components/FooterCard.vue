<template>
  <div class="footer-card-container">
    <ion-card class="footer-card">
      <ion-card-header class="footer-card-header">
        <ion-img :src="require('../assets/media/' + image)" class="footer-card-image" />
        <ion-card-subtitle class="footer-card-source"><a class="link" :href="link">see more</a></ion-card-subtitle>
        <ion-card-title class="footer-card-name">{{ name }}</ion-card-title>
      </ion-card-header>

      <ion-card-content class="footer-card-content"></ion-card-content>
    </ion-card>
  </div>
</template>

<script lang='ts'>
// eslint-disable-next-line @typescript-eslint/no-unused-vars
declare const require: any // typescript needs this, else require() does not have type

import { IonCard, IonCardTitle, IonCardSubtitle, IonCardHeader, IonCardContent, IonImg } from '@ionic/vue';
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'FooterCard',
  components: {
    IonCard,
    IonCardTitle,
    IonCardSubtitle,
    IonCardHeader,
    IonCardContent,
    IonImg
  },
  setup() {
    
    return {}
  },
  props: {
    name: {
      type: String,
      required: true
    },
    image: {
      type: String,
      required: true
    },
    link: {
      type: String,
      required: true
    }
  },
});
</script>

<style scoped lang="scss" src="../assets/style/FooterCardStype.scss"></style>