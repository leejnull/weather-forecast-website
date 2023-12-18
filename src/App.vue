<script setup>
import CitySelector from './components/CitySelector.vue';
</script>

<template>
<div class="main-page">
  <div class="main-content">
    <CitySelector />
  </div>
</div>
</template>

<style scoped lang="scss">

$bigPadding: 64px;
$smallPadding: 48px;

.main-page {
  background-color: #F4F6FA;
  height: calc(100vh - $bigPadding*2);
  width: calc(100vw - $bigPadding*2);
  padding: $bigPadding;
  .main-content {
    background-color: white;
    width: calc(100% - $smallPadding*2);
    height: calc(100% - $smallPadding*2);
    border-radius: 16px;
    padding: $smallPadding;
  }
}

</style>
