<script setup lang="ts">
  import {
    AlertDialogDescription,
    type AlertDialogDescriptionProps,
  } from 'radix-vue'
  import { cn } from '@/utils/index'

  const props = defineProps<AlertDialogDescriptionProps & { class?: string }>()
</script>

<template>
  <AlertDialogDescription
    :class="cn('text-neutral-500 text-sm dark:text-neutral-400', props.class)"
    :as-child="props.asChild"
  >
    <slot />
  </AlertDialogDescription>
</template>
