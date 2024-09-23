<!-- the route link will look like this /products/id -->
<template>
  <div>
    <Head>
      <Title>NuxtStore | {{ products.title }}</Title>
      <Meta name="description" :content="products.description"></Meta>
    </Head>

    <ProductDetails :product="products" />
  </div>
</template>

<script setup>
// the variable id should be the same name in file [id].vue
const { id } = useRoute().params;

const uri = `https://fakestoreapi.com/products/${id}`;
const { data: products } = await useFetch(uri);

// create error msg
if (!products.value) {
  throw createError({
    statusCode: 404,
    statusMessage: "The page you are looking for does not exist",
    fatal: true, // it will throw same error
  });
}

// definePageMeta({
//   // object
//   layout: "products",
// });
</script>
