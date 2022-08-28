<template>
  <ion-page class="presentation-page">
    
    <ion-content class="presentation-content">
    </ion-content>

  </ion-page>
</template>

<script lang="ts">
import { IonContent, IonPage } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'MainPresentation',
  components: {
    IonContent,
    IonPage,
  }
});
</script>

<style scoped lang="scss" src=""></style>