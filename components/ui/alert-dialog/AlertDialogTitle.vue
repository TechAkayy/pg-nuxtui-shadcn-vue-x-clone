<script setup lang="ts">
  import { AlertDialogTitle, type AlertDialogTitleProps } from 'radix-vue'
  import { cn } from '@/utils/index'

  const props = defineProps<AlertDialogTitleProps & { class?: string }>()
</script>

<template>
  <AlertDialogTitle
    :as-child="props.asChild"
    :class="
      cn(
        'text-lg text-neutral-950 font-semibold dark:text-neutral-50',
        props.class,
      )
    "
  >
    <slot />
  </AlertDialogTitle>
</template>
