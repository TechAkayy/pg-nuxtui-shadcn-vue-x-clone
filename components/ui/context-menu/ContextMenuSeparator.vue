<script setup lang="ts">
  import {
    ContextMenuSeparator,
    type ContextMenuSeparatorProps,
  } from 'radix-vue'
  import { cn } from '@/utils/index'

  const props = defineProps<ContextMenuSeparatorProps>()
</script>

<template>
  <ContextMenuSeparator
    v-bind="props"
    :class="
      cn(
        '-mx-1 my-1 h-px bg-neutral-200 dark:bg-neutral-800',
        $attrs.class ?? '',
      )
    "
  />
</template>
