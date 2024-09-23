<template>
  <div>
    <nav
      class="navbar navbar-expand-lg bg-body-tertiary bg-dark border-bottom p-3"
      data-bs-theme="dark"
    >
      <div class="container-fluid">
        <nuxt-link class="navbar-brand fw-bold fs-5" to="/"
          >Mini NuxtStore</nuxt-link
        >
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div
          class="collapse navbar-collapse d-flex justify-content-end me-4"
          id="navbarNav"
        >
          <ul class="navbar-nav fw-bold">
            <li class="nav-item">
              <nuxt-link class="nav-link" aria-current="page" to="/"
                >Home</nuxt-link
              >
            </li>
            <li class="nav-item mx-3">
              <nuxt-link class="nav-link" to="/about">About Us</nuxt-link>
            </li>
            <li class="nav-item">
              <nuxt-link class="nav-link" to="/products">Products</nuxt-link>
            </li>
          </ul>
          <label class="ui-switch ms-4">
            <input type="checkbox" />
            <div class="slider" @click="toggle">
              <div class="circle"></div>
            </div>
          </label>
        </div>
      </div>
    </nav>
  </div>
</template>

<script setup>
const active = ref(false); // Use a reactive reference for state

function toggle() {
  active.value = !active.value; // Toggle the active state

  // alert(active.value);

  if (active.value) {
    document.body.className = "bkg-dark";
  } else {
    document.body.className = "bkg-white";
  }
}
</script>

<style scoped>
/* @import url("~/assets/css/bootstrap.min.css"); */
@import url("~/assets/css/btnswitch.css");
.router-link-exact-active {
  color: #1e9e96 !important;
}
</style>
