<template>
  <div
    class="container d-flex justify-content-center text-center align-items-center vh-100"
  >
    <div class="fw-bold error-content">
      <h1 class="statusCode">{{ error.statusCode }}</h1>
      <h1>Oops!..</h1>
      <p>{{ error.statusMessage }}</p>
      <!-- <a href="/">Go Home</a> -->
      <div class="btn btn-primary" @click="handleClearError">Go Home...</div>
    </div>
  </div>
</template>

<script setup>
defineProps(["error"]);

// const handleClearError = () => clearError({ redirect: "/" });
function handleClearError() {
  clearError({ redirect: "/" });
}
</script>

<style>
.statusCode {
  font-size: 8.5rem;
}
</style>
