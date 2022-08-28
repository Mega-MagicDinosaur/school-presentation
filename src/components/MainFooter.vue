<template>
  <ion-page class="footer-page">
    
    <ion-content class="footer-content" :fullscreen="true">
    </ion-content>

  </ion-page>
</template>

<script lang="ts">
import { IonContent, IonPage } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'MainFooter',
  components: {
    IonContent,
    IonPage,
  }
});
</script>

<style scoped lang="scss" src=""></style>