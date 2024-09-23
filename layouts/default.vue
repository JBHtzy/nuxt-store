<template>
  <div>
    <Navbar />

    <!-- output page content -->
    <div class="container h-100">
      <slot />
      <!-- this is like @yield -->
    </div>

    <Footer />
  </div>
</template>

<script setup lang="ts">
import Navbar from "~/components/Navbar.vue";

const route = useRoute();

watchEffect(() => {
  // updates the title in every diff pages
  useHead({
    title: route.meta.title, // Fallback in case title is missing
  });
});
</script>

<style>
@import url("~/assets/css/style.css");
</style>
