<script setup lang="ts">
  import { SelectSeparator, type SelectSeparatorProps } from 'radix-vue'
  import { cn } from '@/utils/index'

  const props = defineProps<SelectSeparatorProps & { class?: string }>()
</script>

<template>
  <SelectSeparator
    :class="
      cn('-mx-1 my-1 h-px bg-neutral-100 dark:bg-neutral-800', props.class)
    "
  />
</template>
