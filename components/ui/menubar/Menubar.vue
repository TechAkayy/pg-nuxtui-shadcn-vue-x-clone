<script setup lang="ts">
  import {
    MenubarRoot,
    type MenubarRootEmits,
    type MenubarRootProps,
  } from 'radix-vue'
  import { cn } from '@/utils/index'

  const props = defineProps<MenubarRootProps & { class?: string }>()

  const emits = defineEmits<MenubarRootEmits>()
</script>

<template>
  <MenubarRoot
    v-bind="props"
    :class="
      cn(
        'flex h-10 items-center space-x-1 rounded-md border border-neutral-200 border-neutral-200 p-1 dark:border-neutral-800 dark:border-neutral-800',
        props.class,
      )
    "
    @update:model-value="emits('update:modelValue', $event)"
  >
    <slot />
  </MenubarRoot>
</template>
