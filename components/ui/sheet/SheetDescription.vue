<script setup lang="ts">
  import { DialogDescription, type DialogDescriptionProps } from 'radix-vue'
  import { cn } from '@/utils/index'

  const props = defineProps<DialogDescriptionProps & { class?: string }>()
</script>

<template>
  <DialogDescription
    :class="cn('text-sm text-neutral-500 dark:text-neutral-400', props.class)"
    v-bind="props"
  >
    <slot />
  </DialogDescription>
</template>
