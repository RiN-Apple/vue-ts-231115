<template>
  <div>
    <!-- countUpイベントを発行 -->
    <button className="text-4xl" @click="$emit('countUp')">
      +
    </button>
  </div>
</template>