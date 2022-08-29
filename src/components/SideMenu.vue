<template>
  <div class="sidemenu-container">
    
    <div class="sidemenu-button" @click="onSidemenuButtonClick">
      <!-- <div class="bottom-edge"></div> deprecated solution, see stylesheet. -->
    </div>
      
    <div class="page-sidemenu" :class="(sidemenuState)? 'open' : 'closed'">
      <ion-button color="warning" class="sidemenu-close-button"
      @click="onSidemenuButtonClick">
        <ion-icon :icon="add" class="sidemenu-close-icon"></ion-icon>
      </ion-button>

      <div class="navigation-buttons">
        <ion-button expand="full" @click="$emit('navButtonClicked', 0)" class="nav-button">Title</ion-button>
        <ion-button expand="full" @click="$emit('navButtonClicked', 1)" class="nav-button">Presentation</ion-button>
        <ion-button expand="full" @click="$emit('navButtonClicked', 2)" class="nav-button">Credits</ion-button>
      </div>
    </div>

  </div>
</template>

<script lang="ts">
import { IonIcon, IonButton } from '@ionic/vue';
import { defineComponent, ref } from 'vue';

import { add } from 'ionicons/icons';
  
export default defineComponent({
  name: 'SideMenu',
  components: {
    IonIcon, IonButton
  },
  setup() {
    const sidemenuState = ref(false)
    const onSidemenuButtonClick = () => sidemenuState.value = !sidemenuState.value

    return {
      sidemenuState,
      onSidemenuButtonClick,

      add
    }
  }
});
</script>

<style scoped lang="scss" src="../assets/style/SideMenuStyle.scss"></style>