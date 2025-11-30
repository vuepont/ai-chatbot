<script setup lang="ts">
import type { HTMLAttributes } from 'vue'
import { computed, useAttrs } from 'vue'
import { cn } from '@/lib/utils'

const props = defineProps<{
  class?: HTMLAttributes['class']
}>()

const classes = computed(() => cn(
  'flex flex-col overflow-hidden rounded-lg border bg-background shadow-sm',
  props.class,
))
const attrs = useAttrs()
</script>

<template>
  <div
    :class="classes"
    v-bind="attrs"
  >
    <slot />
  </div>
</template>
