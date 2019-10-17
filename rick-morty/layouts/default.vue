<template>
  <main>
    <Header />
    <div class="page">
      <nuxt />
    </div>
  </main>
</template>

<script>
import Header from "~/components/Header.vue";

export default {
  components: {
    Header
  }
};
</script>