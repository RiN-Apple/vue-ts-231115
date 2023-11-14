<script setup lang="ts">
import CountText from './components/CountText.vue'
import CountInput from './components/CountInput.vue'
import CountUpButtton from './components/CountUpButton.vue'

// import Test from './components/Test.vue'
</script>

<template>
  <div class="mx-auto w-1/3">
    <div class="flex flex-col mt-6 text-center">
      <p class="text-3xl">Vue.js </p>
      <CountText />
      <CountInput />
      <CountUpButtton />
      <!-- <Test class="" msg="test"/> -->
    </div>
  </div>
</template>
