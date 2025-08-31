<script setup lang="ts">
import { marked } from 'marked'
const props = defineProps<{
  text: string
}>()
</script>
<template>
  <div id="preview-container">
    <p id="preview">{{ marked.parse(props.text) }}</p>
  </div>
</template>
