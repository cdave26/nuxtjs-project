<template>
    <div>
        <h2>products</h2>
        <div class="grid grid-cols-4 gap-5">
            <div v-for="p in products">
                <NuxtLink :to="`/products/${p.id}`">{{ p.title }}</NuxtLink>
            </div>
        </div>
    </div>
</template>

<script setup>

  definePageMeta({
    layout: 'products'
  })
  const {data: products } = await useFetch('https://api.escuelajs.co/api/v1/products');

</script>