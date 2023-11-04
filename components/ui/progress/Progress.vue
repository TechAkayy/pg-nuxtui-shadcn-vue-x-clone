<script setup lang="ts">
  import {
    ProgressIndicator,
    ProgressRoot,
    type ProgressRootProps,
  } from 'radix-vue'
  import { cn } from '@/utils/index'

  const props = withDefaults(
    defineProps<ProgressRootProps & { class?: string }>(),
    {
      class: '',
      modelValue: 0,
    },
  )
</script>

<template>
  <ProgressRoot
    :class="
      cn(
        'relative h-4 w-full overflow-hidden rounded-full bg-neutral-100 dark:bg-neutral-800',
        props.class,
      )
    "
    v-bind="props"
  >
    <ProgressIndicator
      :class="
        cn(
          'h-full w-full flex-1 duration-300 bg-neutral-950 transition-all dark:bg-neutral-50',
          props.class,
        )
      "
      :style="`transform: translateX(-${100 - (props.modelValue ?? 0)}%);`"
    />
  </ProgressRoot>
</template>
