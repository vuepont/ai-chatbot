<script lang="ts" setup>
import type { HTMLAttributes } from 'vue'
import { BookmarkIcon } from 'lucide-vue-next'
import { useSlots } from 'vue'
import { cn } from '@/lib/utils'

const props = defineProps<{
  class?: HTMLAttributes['class']
}>()

const slots = useSlots()
</script>

<template>
  <slot v-if="slots.default" />

  <BookmarkIcon
    v-else
    :class="cn('size-4 shrink-0', props.class)"
    v-bind="$attrs"
  />
</template>
