<script setup lang="ts">
  import { cn } from '@/utils/index'

  const props = defineProps<{ class?: string }>()
</script>

<template>
  <th
    :class="
      cn(
        'h-12 px-4 text-left align-middle font-medium text-neutral-500 [&:has([role=checkbox])]:pr-0 dark:text-neutral-400',
        props.class,
      )
    "
  >
    <slot />
  </th>
</template>
