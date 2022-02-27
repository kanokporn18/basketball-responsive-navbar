<template>
  <div class="about">
    <NavbarComponent />
    <main class="main">
      <section class="hero">
        <h1>AboutView</h1>
      </section>
    </main>
  </div>
</template>

<script>
import NavbarComponent from '@/components/NavbarComponent.vue';
export default {
  name: 'AboutView',
  components: {
    NavbarComponent,
  },
};
</script>
<style scoped></style>
