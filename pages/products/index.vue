<template>
    <div>
        <h2>products</h2>
        <div class="grid grid-cols-4 gap-5">
            <div v-for="p in products">
             <ProductCards :product="p" /> 
            </div>
        </div>
    </div>
</template>

<script setup>
import ProductCards from '~/components/ProductCards.vue';


  definePageMeta({
    layout: 'products'
  })
  const {data: products } = await useFetch('https://api.escuelajs.co/api/v1/products');

</script>