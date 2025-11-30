<script setup lang="ts">
import { useAttrs } from 'vue'
import { SelectContent } from '@/components/ui/select'

interface Props {
  class?: string
}

const props = defineProps<Props>()
const attrs = useAttrs()
</script>

<template>
  <SelectContent :class="props.class" v-bind="attrs">
    <slot />
  </SelectContent>
</template>
