<script setup lang="ts">
  import { DialogTitle, type DialogTitleProps } from 'radix-vue'
  import { cn } from '@/utils/index'

  const props = defineProps<DialogTitleProps & { class?: string }>()
</script>

<template>
  <DialogTitle
    :class="
      cn(
        'text-lg font-semibold text-neutral-950 dark:text-neutral-50',
        props.class,
      )
    "
    v-bind="props"
  >
    <slot />
  </DialogTitle>
</template>
