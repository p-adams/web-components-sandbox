<script setup lang="ts">
import VTabs from "./v-tabs";
</script>
<template>
  <h3>Tabs Consumer</h3>
  <VTabs>
    <div label="Fruit 1">Apples</div>
    <div label="Fruit 2">Bananas</div>
    <div label="Fruit 3">Pears</div>
  </VTabs>
</template>
<style lang="scss" scoped>
.v-tabs-container {
  margin-top: 20px;
}
</style>
