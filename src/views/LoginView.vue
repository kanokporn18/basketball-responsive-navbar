<template>
  <div class="login">
    <NavbarComponent />
    <main class="main">
      <section class="hero">
        <h1>LoginView</h1>
      </section>
    </main>
  </div>
</template>

<script>
import NavbarComponent from '@/components/NavbarComponent.vue';
export default {
  name: 'LoginView',
  components: {
    NavbarComponent,
  },
};
</script>
<style scoped></style>
