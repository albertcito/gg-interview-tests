<script lang="ts">
export interface Bar {
  title: string;
  color: string;
  currentValue: number;
  previousValue: number;
  currentYear: number;
  previousYear: number;
}
</script>
<script setup lang="ts">
defineProps<Bar>()
</script>

<template>
  <div class="flex flex-col gap-2">
    <h1 class="font-bold">{{ title }}</h1>
    <div class="flex flex-col gap-4">
      <BarsLine :year="previousYear" :width="previousValue" :color="color" />
      <BarsLine :year="currentYear" :width="currentValue" :color="color" />
    </div>
  </div>
</template>