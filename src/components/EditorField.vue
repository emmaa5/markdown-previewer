<script setup lang="ts">
import { ref, type Ref } from 'vue'
import MDRender from './MDRender.vue'

const text: Ref<string> = ref('')
// eslint-disable-next-line @typescript-eslint/no-explicit-any
function onInput(e: any) {
  text.value = e.target.value
}
</script>

<template>
  <div id="editor-container">
    <input id="editor" :value="text" @input="onInput" placeholder="Type here" />
    <MDRender :text="text" />
  </div>
</template>
