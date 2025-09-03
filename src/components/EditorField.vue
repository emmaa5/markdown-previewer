<script setup lang="ts">
// eslint-disable-next-line @typescript-eslint/no-unused-vars
import { ref, type Ref } from 'vue'
import PreviewMD from './PreviewMD.vue'

//const text: Ref<string> = ref('')
//// eslint-disable-next-line @typescript-eslint/no-explicit-any
//function onInput(e: any) {
//  text.value = e.target.value
//}
const inputText = ref('')
</script>

<template>
  <div id="editor-container">
    <textarea id="editor" v-model="inputText" placeholder="Type here" />
    <PreviewMD :text="inputText" />
  </div>
</template>
