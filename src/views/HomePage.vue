<template>
  <ion-page class="home-page">
    <ion-content class="home-content" :fullscreen="true">

      <div class="vertical-scroller">
        <div class="scroller-page" style="background: grey"></div>
        <div class="scroller-page" style="background: grey"></div>
        <div class="scroller-page" style="background: grey"></div>
      </div>
    </ion-content>

  </ion-page>
</template>

<script lang="ts">
import { IonContent, IonPage } from '@ionic/vue';
import { defineComponent } from 'vue';

import MainTitle from '../components/MainTitle.vue';
import MainPresentation from '../components/MainPresentation.vue';
import MainFooter from '../components/MainFooter.vue';

export default defineComponent({
  name: 'HomePage',
  components: {
    IonContent,
    IonPage,
    
  }
});
</script>

<style scoped lang="scss" src="../assets/style/HomePageStyle.scss"></style>
