<script setup lang="ts">
import { type Ref, onMounted, ref } from 'vue'
import Block from '@/components/main-page/Block.vue'
import PopularCars from '@/components/main-page/PopularCars.vue'
import RecomendationCars from '@/components/main-page/RecomendationCars.vue'

import { Api } from '@/api/api'

import type Car from '@/types/cars'

const ApiClass = new Api()

const resp: Ref<Car[]> = ref([])

onMounted(async () => {
  resp.value = await ApiClass.getObjects('all-cars')
  console.log(resp.value)
})
</script>

<template>
  <div class="main-page">
    <div class="ad-blocks">
      <Block
        :background="'/img/main-page/ads-1.png'"
        :header="'The Best Platform for Car Rental'"
        :paragraph="'Ease of doing a car rental safely and reliably. Of course at a low price.'"
        :button-class="'dark-blue'"
      />
      <Block
        :background="'/img/main-page/ads-2.png'"
        :header="'Easy way to rent a car at a low price'"
        :paragraph="'Providing cheap car rental services and safe and comfortable facilities.'"
        :button-class="'light-blue'"
      />
    </div>
    <div class="popular-cars">
      <div class="pc-title">
        <p class="pc-title-common">Popular Cars</p>
        <p class="view-all">View All</p>
      </div>
      <div class="cars-common">
        <PopularCars />
      </div>
    </div>

    <div class="recomendation-cars">
      <div class="rec-cars">
        <p>Recomendation Cars</p>
        <p></p>
      </div>
      <div class="cars-common">
        <RecomendationCars :cars="resp" />
      </div>
    </div>
    <div class="cars-count">
      <p>{{ resp.length }} cars</p>
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
  .popular-cars {
    width: 91.12vw;
    margin-top: 32px;
    display: flex;
    flex-direction: column;

    .pc-title {
      display: flex;
      align-items: center;
      justify-content: space-between;

      .pc-title-common {
        margin: 0;
        padding: 10px 20px;
        color: #90a3bf;
      }
      .view-all {
        margin: 0;
        padding: 10px 20px;
        color: #3563e9;
      }
    }

    .cars-common {
      margin-top: 20px;
      display: flex;
      gap: 32px;
    }
  }

  .recomendation-cars {
    margin-top: 32px;
    width: 91.12vw;
    .rec-cars {
      padding: 10px 20px;
      display: flex;
      align-items: center;
      justify-content: space-between;

      p {
        color: #90a3bf;
      }
    }

    .cars-common {
      margin-top: 20px;
      gap: 32px;
      display: grid;
      grid-template-columns: repeat(4, minmax(0, 1fr));
    }
  }

  .cars-count {
    margin-top: 72px;
    align-self: flex-end;
    p {
      color: #90a3bf;
    }
  }
}
</style>
