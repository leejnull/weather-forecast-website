<template>
<div class="city-selector-content">
  你的城市
  <div style="position: relative;">
    <input 
      class="city-selector-input"
      :value="cityValue"
      @change="e => cityValue = e.target.value"
      @focus="isFocus=true" 
      @blur="isFocus=false"
    />
    <div style="position: absolute;">
      <div class="city-selector-options" :style="{
        opacity: isFocus ? 1 : 0
      }">
        <div 
          v-for="city in cities" 
          :key="city" 
          class="city-selector-option" 
          @click="handleCitySelect(city)"
        >
          {{ city }}
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script setup>
import { ref } from 'vue';


const cities = ['杭州', '上海', '北京']
const isFocus = ref(false)
const cityValue = ref('')

const handleCitySelect = (city) => {
  cityValue.value = city
}

</script>

<style lang="scss" scoped>
$optionHeight: 40px;
.city-selector-content {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  .city-selector-input {
    height: 34px;
    border-radius: 4px;
    border: 1px solid #ECECEC;
    margin-left: 4px;
    padding: 0 6px;
    width: 140px;
    font-size: 14px;
  }
  .city-selector-input:focus {
    outline: 1px solid #FFB400;
  }
  .city-selector-options {
    position: relative;
    width: 152px;
    height: $optionHeight*3;
    left: 4px;
    top: 4px;
    border: 1px solid #ECECEC;
    background-color: white;
    border-radius: 4px;
    display: flex;
    flex-direction: column;
    transition: all 0.3s;
    .city-selector-option {
      height: $optionHeight;
      display: flex;
      align-items: center;
      padding-left: 8px;
      transition: all 0.3s;
    }
    .city-selector-option:hover {
      background-color: #FFC90050;
    }
  }
}
</style>