<script setup lang="ts">
  import { TabsList, type TabsListProps } from 'radix-vue'
  import { cn } from '@/utils/index'

  const props = defineProps<TabsListProps & { class?: string }>()
</script>

<template>
  <TabsList
    v-bind="props"
    :class="
      cn(
        'inline-flex h-10 items-center justify-center rounded-md bg-neutral-100 p-1 text-neutral-500 dark:bg-neutral-800 dark:text-neutral-400',
        props.class,
      )
    "
  >
    <slot />
  </TabsList>
</template>
