<template>
    <button @click="onClick" class="btn">
      <slot />
    </button>
  </template>
  
  <script setup>
  const onClick = () => {
    alert('Button clicked!')
  }
  </script>
  
  <style scoped>
  .btn {
    background-color: #007bff;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
  }
  </style>