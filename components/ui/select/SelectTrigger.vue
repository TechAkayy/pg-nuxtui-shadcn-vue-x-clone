<script setup lang="ts">
  import { SelectIcon, SelectTrigger, type SelectTriggerProps } from 'radix-vue'
  import { ChevronDown } from 'lucide-vue-next'
  import { cn } from '@/utils/index'

  const props = withDefaults(
    defineProps<SelectTriggerProps & { class?: string; invalid?: boolean }>(),
    {
      class: '',
      invalid: false,
    },
  )
</script>

<template>
  <SelectTrigger
    v-bind="props"
    :class="[
      cn(
        'flex h-10 w-full items-center justify-between rounded-md border border-neutral-200 border-neutral-200 bg-white px-3 py-2 text-sm ring-offset-white placeholder:text-neutral-500 focus:outline-none focus:ring-2 focus:ring-neutral-950 focus:ring-offset-2 disabled:cursor-not-allowed disabled:opacity-50 dark:border-neutral-800 dark:border-neutral-800 dark:bg-neutral-950 dark:ring-offset-neutral-950 dark:placeholder:text-neutral-400 dark:focus:ring-neutral-300',
        props.class,
      ),
      props.invalid
        ? '!ring-destructive ring-2 placeholder:!text-destructive'
        : '',
    ]"
  >
    <slot />
    <SelectIcon as-child>
      <ChevronDown class="w-4 h-4 opacity-50" />
    </SelectIcon>
  </SelectTrigger>
</template>
