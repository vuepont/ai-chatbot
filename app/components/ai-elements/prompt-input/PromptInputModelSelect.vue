<script setup lang="ts">
import { useAttrs } from 'vue'
import { Select } from '@/components/ui/select'

const attrs = useAttrs()
</script>

<template>
  <Select v-bind="attrs">
    <slot />
  </Select>
</template>
