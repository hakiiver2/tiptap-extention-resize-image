<script setup lang="ts">
import { useEditor, EditorContent } from '@tiptap/vue-3'
import StarterKit from '@tiptap/starter-kit'
import { ref } from 'vue'
import { ResizableMedia } from './components/resizableMedia'
import { content } from './components/sampleData'

const editor = useEditor({
    content: content,
    extensions: [StarterKit, ResizableMedia],
    editorProps: {
        attributes: {
            class: 'focus:outline-none prose mx-auto',
        },
    },
})
</script>

<template>
  <editor-content :editor="editor" />
</template>

<style scoped>
.logo {
    height: 6em;
    padding: 1.5em;
    will-change: filter;
    transition: filter 300ms;
}
.logo:hover {
    filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
    filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
