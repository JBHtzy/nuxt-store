<template>
  <div>
    <header class="mt-3">
      <h2>{{ product.title }}</h2>
      <span class="fst-italic">{{ product.category }}</span>
    </header>

    <div class="card mt-5" style="max-width: 100%">
      <div class="row g-6">
        <div class="col-md-4">
          <img
            :src="product.image"
            class="img-fluid object-fit-contain border rounded rounded-start"
            alt="..."
          />
        </div>
        <div class="col-md-8">
          <div class="card-body">
            <h3 class="card-title">{{ product.title }}</h3>
            <div class="caption-top">Description:</div>
            <p class="card-text">
              {{ product.description }}
            </p>
            <p class="card-text">
              <small class="text-body-secondary">Last updated 3 mins ago</small>
            </p>
            <hr />
            <h4 class="fw-bold">₱ {{ product.price }}</h4>
            <nuxt-link to="#" class="btn btn-success mt-3"
              ><i class="fa-solid fa-cart-shopping"></i> Add to Card</nuxt-link
            >
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const { product } = defineProps(["product"]);
</script>

<style>
img {
  width: 70%;
  margin: 0 auto;
}
</style>
