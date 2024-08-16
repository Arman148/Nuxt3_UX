<template>
    <div>
      <Header :title="headerTitle" />
      <main>
        <slot />
      </main>
      <footer>
        <p>This is the footer</p>
      </footer>
    </div>
  </template>
  
  <style>
  header, footer {
    text-align: center;
    padding: 10px;
    background-color: #f5f5f5;
  }
  </style>

<script setup>
    import { content } from '~/assets/content.js';
    import Header from '@/components/Header.vue';

    const headerTitle = content.headerTitle;

</script>
  