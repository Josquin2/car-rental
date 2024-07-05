<script setup lang="ts">
import { defineProps } from 'vue'

const props = defineProps({
  name: String,
  type: String,
  photo: String,
  fuel_tank: String,
  transmission: String,
  people: String,
  price: Number
})
</script>

<template>
  <div class="one-car">
    <div class="car-header">
      <div class="car-name">
        <h3>{{ props.name }}</h3>
        <p>{{ props.type }}</p>
      </div>
      <div class="heart">
        <span class="heart-default"></span>
      </div>
    </div>
    <div class="car-photo">
      <img :src="props.photo" alt="" />
    </div>
    <div class="car-info">
      <div class="one-desc">
        <img src="/icons/car/gas.png" alt="" />
        <p>{{ props.fuel_tank }}</p>
      </div>

      <div class="one-desc">
        <img src="/icons/car/transmission.png" alt="" />
        <p>{{ props.transmission }}</p>
      </div>

      <div class="one-desc">
        <img src="/icons/car/people.png" alt="" />
        <p>{{ props.people }}</p>
      </div>
    </div>
    <div class="car-price">
      <div class="price-common">
        <h4>${{ props.price }}.00/</h4>
        <p>day</p>
      </div>
      <button class="rent-button">Rent Now</button>
    </div>
  </div>
</template>

<style lang="scss">
.one-car {
  width: 304px;
  height: 388px;
  border: none;
  border-radius: 10px;
  padding: 24px;
  background-color: #ffffff;
  display: flex;
  flex-direction: column;

  * {
    background-color: #ffffff;
  }

  .car-header {
    display: flex;
    align-items: flex-start;
    justify-content: space-between;
    .car-name {
      cursor: pointer;
      p {
        font-size: 14px;
        color: #90a3bf;
      }
    }
    .heart {
      .heart-default {
        cursor: pointer;
        display: flex;
        align-items: center;
        justify-content: center;
        width: 24px;
        height: 24px;
        background: url('/icons/car/like.png');
      }

      .heart-clicked {
        background: url('/icons/car/like-clicked.png');
      }
    }
  }
  .car-photo {
    cursor: pointer;
    margin-top: 64px;
    align-self: center;
    width: 232px;
    height: 72px;

    img {
      position: absolute;
    }
  }

  .car-info {
    align-self: center;
    margin-top: 64px;
    display: flex;
    gap: 16px;

    .one-desc {
      gap: 4px;
      display: flex;
      align-items: center;

      p {
        font-size: 14px;
        color: #90a3bf;
      }
    }
  }
  .car-price {
    margin-top: 24px;
    display: flex;
    align-items: center;
    justify-content: space-between;

    .price-common {
      display: flex;
      align-items: center;
      h4 {
        margin: 0;
        font-size: 20px;
      }
      p {
        margin: 0;
        margin-left: 4px;
        margin-top: 4px;
        font-size: 14px;
        color: #90a3bf;
      }
    }

    .rent-button {
      cursor: pointer;
      height: 44px;
      width: 116px;
      border: none;
      border-radius: 4px;
      background-color: #3563e9;
      font-size: 16px;
      color: #ffffff;
    }
  }
}
</style>
