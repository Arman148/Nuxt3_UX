<template>
  <footer class="footer">
    <div class="footer-content">
      <p class="footer-title">{{ footerTitle }}</p>
      <div class="contacts">
        <div v-for="(contact, index) in contacts" :key="index">
          <span v-if="contact.type === 'phone'" class="contact phone">{{ contact.value }}</span>
          <span v-if="contact.type === 'email'" class="contact email">{{ contact.value }}</span>
        </div>
      </div>
      <img :src="logo" alt="Logo" class="footer-logo" />
    </div>
  </footer>
</template>

<script setup>
const props = defineProps({
  contacts: {
    type: Array,
    required: true,
    default: () => [],
  },
  logo: {
    type: String,
    required: true,
  },
  footerTitle: {
    type: String,
    required: true,
  },
});
</script>

<style lang="scss" scoped>
.footer {
  background: linear-gradient(90deg, #3d2e80, #dc1969);
  padding: 40px;
  text-align: center;
  color: white;

  .footer-content {
    max-width: 1440px;
    margin: 0 auto;

    .footer-title {
      font-family: 'Mulish', sans-serif;
      font-size: 48px;
      font-weight: 900;
      line-height: 59px;
      text-align: center;
      margin-bottom: 20px;
    }

    .contacts {
      margin-bottom: 20px;

      .contact {
        display: block;
        margin: 5px 0;
        font-family: 'Muli', sans-serif;
        font-size: 30px;
        font-weight: 700;
        line-height: 40px;

        &.phone {
          color: white;
        }

        &.email {
          color: #dc1969;
        }
      }
    }

    .footer-logo {
      width: 274px;
      height: 44px;
      margin: 20px auto;
    }
  }

  // Responsive design for smaller devices
  @media (max-width: 767px) {
    .footer-content {
      .footer-title {
        font-size: 24px;
        line-height: 34px;
      }

      .contacts {
        .contact {
          font-size: 22px;
          line-height: 40px;
          text-align: center;
        }
      }

      .footer-logo {
        width: 144.47px;
        height: 23px;
      }
    }
  }
}
</style>
