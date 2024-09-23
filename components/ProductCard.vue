<template>
  <div>
    <div
      class="card d-flex justify-content-center text-center align-items-center flex-column p-3"
    >
      <img
        :src="product.image"
        class="card-img-top thumb object-fit-contain border rounded"
        alt="..."
      />
      <div class="card-body">
        <p class="card-text">Category: {{ product.category }}</p>
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
.card {
  height: 265px;
}

.thumb {
  max-height: 120px;
  max-width: 70%;
  margin: 0 auto;
}
</style>
