<script setup lang="ts">
  import {
    DropdownMenuSeparator,
    type DropdownMenuSeparatorProps,
  } from 'radix-vue'

  const props = defineProps<DropdownMenuSeparatorProps>()
</script>

<template>
  <DropdownMenuSeparator
    v-bind="props"
    class="-mx-1 my-1 h-px bg-neutral-100 dark:bg-neutral-800"
  />
</template>
