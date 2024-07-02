<script setup lang="ts">
import Block from '@/components/main-page/Block.vue'
</script>

<template>
  <div class="main-page">
    <div class="ad-blocks">
      <Block
        :background="'/public/img/main-page/ads-1.png'"
        :header="'The Best Platform for Car Rental'"
        :paragraph="'Ease of doing a car rental safely and reliably. Of course at a low price.'"
        :button-class="'dark-blue'"
      />
      <Block
        :background="'/public/img/main-page/ads-2.png'"
        :header="'Easy way to rent a car at a low price'"
        :paragraph="'Providing cheap car rental services and safe and comfortable facilities.'"
        :button-class="'light-blue'"
      />
    </div>
  </div>
</template>

<style lang="scss">
.main-page {
  margin-top: 32px;
  padding: 0 4.44vw;
  min-height: 60vh;
  display: flex;
  flex-direction: column;
  align-items: center;

  .ad-blocks {
    display: flex;
    gap: 32px;
  }
}
</style>
