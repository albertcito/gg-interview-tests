<script setup lang="ts">
defineProps<{
  year: number;
  width: number;
  color: string;
}>()
</script>

<template>
  <div class="bg-neutral-200 dark:bg-neutral-800 rounded-lg">
    <div class="rounded-lg">
      <div class="px-1 rounded-full text-white text-sm overflow-auto whitespace-nowrap">
        {{ year }} - {{ width }}%
      </div>
    </div>
  </div>
</template>