<script setup lang="ts">
  import type { SliderRootEmits, SliderRootProps } from 'radix-vue'
  import {
    SliderRange,
    SliderRoot,
    SliderThumb,
    SliderTrack,
    useEmitAsProps,
  } from 'radix-vue'
  import { cn } from '@/utils/index'

  const props = defineProps<SliderRootProps>()
  const emits = defineEmits<SliderRootEmits>()

  const emitsAsProps = useEmitAsProps(emits)
</script>

<template>
  <SliderRoot
    :class="
      cn(
        'relative flex w-full touch-none select-none items-center',
        $attrs.class ?? '',
      )
    "
    v-bind="{ ...props, ...emitsAsProps }"
  >
    <SliderTrack
      class="relative h-2 w-full grow overflow-hidden rounded-full bg-neutral-100 dark:bg-neutral-800"
    >
      <SliderRange class="absolute h-full bg-neutral-900 dark:bg-neutral-50" />
    </SliderTrack>
    <SliderThumb
      class="block h-5 w-5 rounded-full border-2 border-neutral-900 bg-white ring-offset-white transition-colors focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-neutral-950 focus-visible:ring-offset-2 disabled:pointer-events-none disabled:opacity-50 dark:border-neutral-50 dark:bg-neutral-950 dark:ring-offset-neutral-950 dark:focus-visible:ring-neutral-300"
    />
  </SliderRoot>
</template>
