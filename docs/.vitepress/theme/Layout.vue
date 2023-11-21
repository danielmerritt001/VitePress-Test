<script setup>
import { useData } from 'vitepress'

// https://vitepress.dev/reference/runtime-api#usedata
const { site, frontmatter } = useData()
console.log(useData())
</script>

<template>
  <nav>
    <a href="/">Home</a>
    <a href="/markdown-examples.html">Markdown Examples</a> 
    <a href="/api-examples.html">API Examples</a>
    <a href="/test.html">Test</a>
    <a href="/about">About</a>
  </nav>
  <div v-if="frontmatter.home">
    <div class="header">
      <h1 class="header__title">{{ site.title }}</h1>
      <p class="header__intro">{{ site.description }}</p>
    </div>
    
  </div>
  <div v-else>
    <Content />
  </div>
</template>
