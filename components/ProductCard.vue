<template>
  <div>
    <div
      class="card h-100 d-flex justify-content-center text-center align-items-center flex-column"
    >
      <img
        :src="product.image"
        class="card-img-top thumb object-fit-contain border rounded"
        alt="..."
      />
      <div class="card-body">
        <!-- <h5 class="card-title">{{ product.title }}</h5>
        <p class="card-text">Price: {{ product.price }}</p> -->
        <p class="card-text">Category: {{ product.category }}</p>
        <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
        <nuxt-link :to="`/products/${product.id}`" class="btn btn-primary"
          ><i class="fa-solid fa-arrow-up-right-from-square"></i> View
          Details</nuxt-link
        >
      </div>
    </div>
  </div>
</template>

<script setup>
const { product } = defineProps(["product"]);
</script>

<style>
.thumb {
  max-height: 120px;
  max-width: 70%;
  margin: 0 auto;
}
</style>
