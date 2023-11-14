<script setup lang="ts">
// バケツリレー
defineProps({
  count: Number,
  isTextColorRed: Boolean
});
</script>

<template>
  <div className="py-32">
    <p :class="[`text-8xl`, isTextColorRed ? `text-red-600`:`text-black`]" >
    <!-- Propsが更新されると再レンダリングが発生する -->
    {{ count }}
    </p>
</div>
</template>