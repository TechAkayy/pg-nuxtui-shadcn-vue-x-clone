<script setup lang="ts">
  import { cn } from '@/utils/index'
</script>

<template>
  <span
    :class="
      cn('text-xxs ml-auto tracking-widest opacity-50', $attrs.class ?? '')
    "
  >
    <slot />
  </span>
</template>
