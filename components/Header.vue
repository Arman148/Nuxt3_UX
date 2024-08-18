<template>
  <header class="header">
    <div class="header-content">
      <div class="header-top">
        <img :src="logo" alt="Logo" class="header-logo" />
        <ReusableButton :text="buttonText" :clickHandler="buttonAction" />
      </div>
      <h1 class="header-title">{{ headerTitle }}</h1>
    </div>
  </header>
</template>

<script setup>
import ReusableButton from '~/components/ReusableButton.vue';

const props = defineProps({
  logo: {
    type: String,
    required: true,
  },
  headerTitle: {
    type: String,
    required: true,
  },
  buttonText: {
    type: String,
    required: true,
  },
  buttonAction: {
    type: Function,
    default: () => alert('Button clicked!'), // Default action
  },
});
</script>

<style lang="scss" scoped>
.header {
  width: 100%;
  background: linear-gradient(159.13deg, #3d2e80 51.38%, #dc1969 125.72%);
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0;
  margin: 0;
  box-sizing: border-box;

  // Responsive heights
  height: 554px;

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
  max-width: 1440px; // Match footer width
  text-align: center;
  padding: 0 20px; // Padding for smaller screens

  @media (max-width: 768px) {
    padding: 0;
  }
}

.header-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  padding: 0 20px;

  @media (max-width: 768px) {
    flex-direction: column;
    align-items: center;
  }
}

.header-logo {
  width: 145px;
  height: auto;

  @media (max-width: 768px) {
    margin-bottom: 20px;
  }
}

.header-title {
  font-family: 'Mulish', sans-serif;
  font-size: 50px;
  font-weight: 900;
  color: #ffffff;
  margin-top: 20px;

  @media (max-width: 1024px) {
    font-size: 40px;
  }

  @media (max-width: 768px) {
    font-size: 30px;
  }
}

.reusable-button {
  width: 200px;
  height: 42px;
  margin-top: 20px;

  @media (max-width: 768px) {
    margin-top: 20px;
  }
}
</style>
