<template>
  <div class="home">
    <NavbarComponent />
    <main class="main">
      <section class="hero">
        <h1>HomeView</h1>
      </section>
    </main>
  </div>
</template>

<script>
import NavbarComponent from '@/components/NavbarComponent.vue';
export default {
  name: 'HomeView',
  components: {
    NavbarComponent,
  },
};
</script>
<style scoped></style>
