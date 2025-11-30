<script setup lang="ts">
import { useAttrs } from 'vue'
import { SelectValue } from '@/components/ui/select'

interface Props {
  class?: string
}

const props = defineProps<Props>()
const attrs = useAttrs()
</script>

<template>
  <SelectValue :class="props.class" v-bind="attrs" />
</template>
