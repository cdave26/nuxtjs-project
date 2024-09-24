<template>
    <div> 
        <Head>
            <Title> Nuxt Dojo | {{ product.title  }}</Title>
            <Meta name="description" :content="product.description"/>
        </Head>
        <ProductDetails :product="product"/>
    </div>
</template>

<script setup>
import ProductDetails from '~/components/ProductDetails.vue';

        const {id} = useRoute().params;
        const uri = 'https://api.escuelajs.co/api/v1/products/' + id;

        // fetch the product 
        const {data: product} = await useFetch(uri, {key: id});
        if(!product.value){
            throw createError({ statusCode: 404, statusMessage: 'Product Not Found', fatal: true})
        }
</script>

<style lang="scss" scoped>

</style>