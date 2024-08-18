<template>
  <button @click="clickHandler" class="reusable-button">
    {{ text }}
  </button>
</template>

<script setup>
const props = defineProps({
  text: {
    type: String,
    required: true,
  },
  clickHandler: {
    type: Function,
    required: true,
  },
});
</script>

<style lang="scss">
.reusable-button {
  width: 200px;
  height: 42px;
  background-color: #ee325c;
  color: #ffffff;
  font-family: 'Mulish', sans-serif;
  font-size: 14px;
  font-weight: 900;
  text-align: center;
  line-height: 42px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;

  &:hover {
    background-color: #d31b53;
  }

  @media (max-width: 768px) {
    width: 180px;
    height: 38px;
    font-size: 13px;
    line-height: 38px;
  }
}
</style>
