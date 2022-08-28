<template>
  <div class="title-page">
    
    <div class="title-content">
      <div class="title-container" :class="(titleDropdownState)? 'active' : 'inactive'" 
      @click="onTitleContainerClick">
        <span class="title">PCTO</span>
      </div>

      <div class="title-dropdown" :class="(titleDropdownState)? 'open' : 'closed'">
        <span class="dropdown-title"></span>
        <span class="dropdown-paragraph"></span>
      </div>
    </div>

  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';

export default defineComponent({
  name: 'MainTitle',
  components: {},
  setup() {
    const titleDropdownState = ref(false)
    const onTitleContainerClick = () => titleDropdownState.value = !titleDropdownState.value

    return {
      onTitleContainerClick,
      titleDropdownState
    }
  }
});
</script>

<style scoped lang="scss" src="../assets/style/MainTitleStyle.scss"></style>