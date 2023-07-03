<template>
  <div v-html="parsed">
  </div>
</template>
<script setup>
import { ref } from 'vue'
import MarkdownIt from 'markdown-it'

const md = new MarkdownIt('default', {
    html: true,
    linkify: true,
    breaks: false
  })

const markdown = 'https://modrinth.com'

const parsed = ref(md.render(markdown))
</script>