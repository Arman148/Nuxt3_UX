<template>
  <header class="header">
    <div class="header-content">
      <img src="@/assets/logo.svg" alt="Logo" class="header-logo" />
      <h1 class="header-title">{{ title }}</h1>
      <button class="header-button">Click Me</button>
    </div>
  </header>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    required: true
  }
});
</script>

<style scoped lang="scss">
.header {
  width: 100%;
  height: 554px;
  background: linear-gradient(159.13deg, #3D2E80 51.38%, #DC1969 125.72%);
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  padding: 20px;

  @media (max-width: 1024px) {
    height: 400px;
  }

  @media (max-width: 768px) {
    height: auto;
    padding: 40px 20px;
  }
}

.header-content {
  width: 100%;
  max-width: 694px;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;

  @media (max-width: 768px) {
    max-width: 100%;
  }
}

.header-logo {
  width: 100px; /* Adjust size as needed */
  height: auto;
  margin-bottom: 20px; /* Space between logo and title */
}

.header-title {
  font-family: 'Mulish', sans-serif;
  font-size: 50px;
  font-weight: 900;
  line-height: 1.2;
  color: #ffffff;
  margin-bottom: 20px;

  @media (max-width: 1024px) {
    font-size: 40px;
    line-height: 1.1;
  }

  @media (max-width: 768px) {
    font-size: 32px;
  }
}

.header-button {
  width: 200px;
  height: 42px;
  background-color: #EE325C;
  color: #ffffff;
  font-family: 'Mulish', sans-serif;
  font-size: 14px;
  font-weight: 900;
  text-align: center;
  line-height: 42px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  margin-top: 30px;
  transition: background-color 0.3s ease;

  &:hover {
    background-color: #D31B53;
  }

  @media (max-width: 768px) {
    width: 180px;
    height: 38px;
    font-size: 13px;
    line-height: 38px;
  }
}
</style>
