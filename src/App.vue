<script setup lang="ts">
import CountText from './components/CountText.vue'
import CountInput from './components/CountInput.vue'
import CountUpButtton from './components/CountUpButton.vue'
import { Ref, computed, ref } from 'vue';

// refで状態を管理
const count: Ref<number> = ref(0);
// refの変更に合わせて更新される算出プロパティ
const isTextColorRed = computed(() => {
  return count.value >= 5 ? true : false
})

// countを+1する
const countUp = () => {
  // count.valueでアクセス
  count.value++;
}
</script>

<template>
  <div class="mx-auto w-1/3">
    <div class="flex flex-col mt-6 text-center">
      <p class="text-3xl">Vue.js </p>
      <!-- v-bind で値を渡す -->
      <CountText v-bind:count="count" v-bind:is-text-color-red="isTextColorRed"/>
      <!-- イベントを受け取ったら関数を実行-->
      <CountInput v-model="count" />
      <CountUpButtton @countUp="countUp" />
      <!-- v-if="count > 15"でも実現可能 -->
      <!-- 使い分け https://qiita.com/aqua_ix/items/61eac355f3c24d7676e1-->
      <p v-show="count > 15">たくさん押したね♬</p>
    </div>
  </div>
</template>
