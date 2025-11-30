<script setup lang="ts">
import { useAttrs } from 'vue'
import { SelectItem } from '@/components/ui/select'

interface Props {
  class?: string
  value: string | number
}

const props = defineProps<Props>()
const attrs = useAttrs()
</script>

<template>
  <SelectItem :class="props.class" :value="props.value" v-bind="attrs">
    <slot />
  </SelectItem>
</template>
