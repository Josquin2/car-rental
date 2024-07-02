<script setup lang="ts">
import { defineProps } from 'vue'

const props = defineProps({
  background: String,
  header: String,
  paragraph: String,
  buttonClass: String
})
</script>

<template>
  <div class="one-big-block">
    <img :src="props.background" alt="" class="background" />
    <div class="info">
      <h2>{{ props.header }}</h2>
      <p>{{ props.paragraph }}</p>
      <button :class="props.buttonClass">Rental Car</button>
    </div>
  </div>
</template>

<style lang="scss">
.one-big-block {
  width: 640px;
  height: 360px;

  .background {
    position: absolute;
    z-index: 1;
  }
  .info {
    position: absolute;
    z-index: 2;
    background: transparent !important;
    font-synthesis: none;
    padding: 24px;
    h2,
    p {
      background: transparent !important;
      color: #ffffff;
    }

    h2 {
      font-size: 32px;
      font-weight: 400;
      max-width: 272px;
    }

    p {
      margin-top: 16px;
      max-width: 284px;
    }

    button {
      cursor: pointer;
      margin-top: 20px;
      width: 120px;
      height: 44px;
      border: none;
      border-radius: 5px;
      font-weight: 500;
      font-size: 16px;
      color: #ffffff;
    }
    .dark-blue {
      background-color: #3563e9;
    }
    .light-blue {
      background-color: #54a6ff;
    }
  }
}
</style>
