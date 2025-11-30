<script setup lang="ts">
import type { HTMLAttributes } from 'vue'
import { computed, useAttrs } from 'vue'
import { cn } from '@/lib/utils'

const props = defineProps<{
  class?: HTMLAttributes['class']
}>()

const classes = computed(() => cn('font-medium text-foreground text-sm', props.class))
const attrs = useAttrs()
</script>

<template>
  <p
    v-bind="attrs"
    :class="classes"
  >
    <slot />
  </p>
</template>
