<template>
  <div>
    <div
      class="vh-100 d-flex justify-content-center align-items-center flex-column"
      v-if="status === 'pending'"
    >
      <div class="lds-ellipsis">
        <div></div>
        <div></div>
        <div></div>
        <div></div>
      </div>
      <span class="fw-bold fst-italic">Loading...</span>
    </div>
    <div v-else>
      <h2 class="my-3">Products Page</h2>

      <div class="row row-cols-1 row-cols-md-4 g-2 g-lg-3">
        <div class="col" v-for="p in products" :key="p.id">
          <ProductCard :product="p" />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import ProductCard from "~/components/ProductCard.vue";

definePageMeta({
  title: "NuxtStore | Products",
  // layout: "products",
});

const { status, data: products } = await useLazyFetch(
  "https://fakestoreapi.com/products"
); // fetching data

if (!products.value) {
  throw createError({
    statusCode: 404,
    statusMessage: "Failed to fetch products.",
    fatal: true,
  });
}
</script>

<style>
@import url("~/assets/css/loading.css");
</style>
