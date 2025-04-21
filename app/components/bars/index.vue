<script setup lang="ts">
import type { Bar } from "./bar.vue";

defineProps<{ bars: Bar[] }>();
</script>

<template>
  <div class="flex flex-col gap-4 p-4">
    <BarsBar
      v-for="bar in bars"
      :key="bar.title"
      :title="bar.title"
      :color="bar.color"
      :current-value="bar.currentValue"
      :previous-value="bar.previousValue"
      :current-year="bar.currentYear"
      :previous-year="bar.previousYear"
    />
  </div>
</template>