<template>
  <div>
    <Header
      :logo="logoUX_Design"
      :headerTitle="headerTitle"
      :buttonText="buttonText"
      :buttonAction="buttonAction"
    />
    <main>
      <slot />
    </main>
    <Footer
      :logo="logoRiesenia"
      :contacts="contacts"
      :footerTitle="footerTitle"
    />
  </div>
</template>

<script setup>
import { content } from '~/assets/content.js';
import Header from '~/components/Header.vue';
import Footer from '~/components/Footer.vue'; // Import footer component

// Example of dynamic values
const logoUX_Design = content.logoUX_Design;
const logoRiesenia = content.logoRiesenia;

const headerTitle = content.headerTitle;
const buttonText = content.buttonText;

const footerTitle = content.footerTitle;
const contacts = content.contacts;

// Optional: Custom button action for each page
const buttonAction = () => {
  alert('This is a custom action for the button on this page!');
};
</script>
