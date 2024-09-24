<template>
    <div>
        <ProductDetails :product="product"/>
    </div>
</template>

<script setup>
import ProductDetails from '~/components/ProductDetails.vue';

        const {id} = useRoute().params;
        const uri = 'https://api.escuelajs.co/api/v1/products/' + id;

        // fetch the product 
        const {data: product} = await useFetch(uri, {key: id});
</script>

<style lang="scss" scoped>

</style>