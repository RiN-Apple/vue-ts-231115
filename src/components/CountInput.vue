<script setup lang="ts">
</script>

<template>
  <div>
    <!-- $emitで単方向(子->親) -->
    <!-- ※v-modelを使うと双方向(状態<->テキストフィールド)が実現できます-->
    <input
      type="text"
      name="count"
      className="border border-gray-400 p-1"
      @input="$emit('update:modelValue', $event.target.value)"
    />
  </div>
</template>