<template>
  <svg :width="width" :height="height">
    <use :xlink:href="createXlinkHref" />
  </svg>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
  width: {
    required: true,
  },
  height: {
    required: true,
  },
  name: {
    required: true,
  },
})

const createXlinkHref = computed(() => `#${props.name}_icon`)
</script>