<script setup lang="ts">
import { ref } from "@vue/reactivity";
import CodeSnippet from "../components/v-snippet.vue";
const count = ref(0);
const markup = ` 
    <script>
      import { ref } from "@vue/reactivity";
      const count = ref(0);
    <script>
    <template>
      <h3>Counter App</h3>
      <div class="counter-wrapper">
        <p>{{ count }}</p>
        <div class="counter-actions">
          <button @click='count--'>-</button>
          <button @click='count++'>+</button>
        </div>
      </div>
    </template>
    `;
</script>

<template>
  <h3>Counter App</h3>
  <div class="counter-wrapper">
    <p>{{ count }}</p>
    <div class="counter-actions">
      <button @click="count--">-</button>
      <button @click="count++">+</button>
    </div>
  </div>
  <CodeSnippet :snippet="markup" />
</template>

<style lang="scss" scoped>
h3 {
  text-transform: uppercase;
  margin-bottom: 20px;
}
.counter-wrapper {
  display: flex;
  flex-direction: column;

  p {
    text-align: center;
    font-size: 32px;
    margin-bottom: 20px;
  }
  .counter-actions {
    display: flex;
    width: 200px;
    button {
      margin: 10px;
      width: 130px;
    }
  }
}
.code-snippet {
  border: 1px solid lightgray;
  border-radius: 8px;
  padding: 10px;
  margin-top: 10px;
}
</style>
