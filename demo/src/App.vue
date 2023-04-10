<script setup>
import { useEditor, EditorContent } from '@tiptap/vue-3'
import StarterKit from '@tiptap/starter-kit'
import { ref } from 'vue';
import { ResizableMedia } from '../../src/components/resizableMedia'
import { content } from './sampleData'

const editor = useEditor({
  content: content,
  extensions: [
    StarterKit,
    ResizableMedia,
  ],
  editorProps: {
    attributes: {
      class: 'focus:outline-none prose mx-auto'
    }
  }
})

</script>

<template>
    <editor-content :editor="editor" />
</template>

<style scoped>
</style>
