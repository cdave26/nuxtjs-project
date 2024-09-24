<template>
    <div class="card text-center">
        <img :src="product.category.image" alt="test" class="thumb">
        <p class="font-bold text-gray truncate m-4">{{ product.title }}</p>
        <NuxtLink :to="`/products/${product.id}`">
            <p class="btn"> View Details</p>
        </NuxtLink>
    </div>
</template>

<script setup>
 const { product } = defineProps(['product']);
</script>

<style lang="scss" scoped>

</style>