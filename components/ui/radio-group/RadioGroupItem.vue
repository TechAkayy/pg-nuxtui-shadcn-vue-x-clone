<script setup lang="ts">
  import {
    RadioGroupIndicator,
    RadioGroupItem,
    type RadioGroupItemProps,
  } from 'radix-vue'
  import { Circle } from 'lucide-vue-next'
  import { cn } from '@/utils/index'

  const props = defineProps<RadioGroupItemProps & { class?: string }>()
</script>

<template>
  <RadioGroupItem
    v-bind="props"
    :class="
      cn(
        'aspect-square h-4 w-4 rounded-full cursor-pointer flex justify-center items-center border border-neutral-200 border-neutral-900 disabled:cursor-not-allowed disabled:opacity-50 dark:border-neutral-800 dark:border-neutral-50',
        props.class,
      )
    "
  >
    <RadioGroupIndicator
      :class="cn('flex items-center justify-center', props.class)"
    >
      <Circle class="w-2.5 h-2.5 text-neutral-950 dark:text-neutral-50" />
    </RadioGroupIndicator>
  </RadioGroupItem>
</template>
