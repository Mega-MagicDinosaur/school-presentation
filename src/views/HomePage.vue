<template>
  <ion-page class="home-page">
    
    <ion-content class="home-content" :fullscreen="true">

      <side-menu style="z-index: 3;" @navButtonClicked="onNavButtonClicked" />

      <div class="vertical-scroller" :class="'page-' + currentPage">

        <div class="scroller-page" style=""> <main-title /> </div>

        <ion-button color="warning" 
        class="scroller-button" :class="(currentPage == 1)? 'up' : 'down'"
        @click="onScrollerButtonClick([0, 1])">
          <ion-icon :icon="chevronDown" class="scroller-button-icon"></ion-icon>
        </ion-button>

        <div class="scroller-page"> <main-presentation style=""/> </div>

        <ion-button color="warning" 
        class="scroller-button" :class="(currentPage == 2)? 'up' : 'down'"
        @click="onScrollerButtonClick([1, 2])">
          <ion-icon :icon="chevronDown" class="scroller-button-icon"></ion-icon>
        </ion-button>

        <div class="scroller-page"> <main-footer /> </div>
      </div>

    </ion-content>

  </ion-page>
</template>

<script lang="ts">
import { IonContent, IonPage, IonIcon, IonButton } from '@ionic/vue';
import { defineComponent, ref } from 'vue';

import { chevronDown } from 'ionicons/icons';

import MainTitle from '../components/MainTitle.vue';
import MainPresentation from '../components/MainPresentation.vue';
import MainFooter from '../components/MainFooter.vue';
import SideMenu from '../components/SideMenu.vue'

export default defineComponent({
  name: 'HomePage',
  components: {
    IonContent,
    IonPage,
    MainTitle,
    MainPresentation,
    MainFooter,
    IonIcon,
    IonButton,
    SideMenu
  },
  setup() {
    const currentPage = ref(0)
    const onScrollerButtonClick = (bridge: [number, number]) => { 
      currentPage.value = 
      (bridge[0] == currentPage.value)? bridge[1] : 
      (bridge[1] == currentPage.value)? bridge[0] : 
      currentPage.value;
    }
    const onNavButtonClicked = (index: number) => currentPage.value = index

    return {
      currentPage,
      onScrollerButtonClick,
      onNavButtonClicked,

      // icons
      chevronDown,
    }
  }
});
</script>

<style scoped lang="scss" src="../assets/style/HomePageStyle.scss"></style>
