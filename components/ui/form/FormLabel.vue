<script lang="ts" setup>
  import { useAttrs } from 'vue'
  import { Label, type LabelProps } from 'radix-vue'
  import { useFormField } from './useFormField'
  import { cn } from '@/utils/index'

  defineOptions({
    inheritAttrs: false,
  })
  const props = defineProps<LabelProps>()

  const { error, formItemId } = useFormField()
  const { class: className, ...rest } = useAttrs()
</script>

<template>
  <Label
    :class="
      cn(
        'block text-sm tracking-tight font-medium text-neutral-950 text-left dark:text-neutral-50',
        error && 'text-red-500 dark:text-red-900',
        className ?? '',
      )
    "
    :for="formItemId"
    v-bind="rest"
  >
    <slot />
  </Label>
</template>
