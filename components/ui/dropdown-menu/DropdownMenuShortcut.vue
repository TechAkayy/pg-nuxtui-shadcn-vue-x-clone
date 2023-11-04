<script setup lang="ts">
  import { cn } from '@/utils/index'
</script>

<template>
  <span
    :class="
      cn('ml-auto text-xs tracking-widest opacity-60', $attrs.class ?? '')
    "
  >
    <slot />
  </span>
</template>
