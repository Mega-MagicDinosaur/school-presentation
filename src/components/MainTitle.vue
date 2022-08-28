<template>
  <ion-page class="title-page">
    
    <ion-content class="title-content">
      <div class="title-container">
        <span class="title">PCTO EXPO</span>
      </div>
    </ion-content>

  </ion-page>
</template>

<script lang="ts">
import { IonContent, IonPage } from '@ionic/vue';
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'MainTitle',
  components: {
    IonContent,
    IonPage,
  }
});
</script>

<style scoped lang="scss" src="../assets/style/MainTitleStyle.scss"></style>