<template>
    <div>
        <p>{{ product.title }}</p>
        <p>{{ product.price }}</p>
        <p>{{ product.id }}</p>
    </div>
</template>

<script setup>
        const {id} = useRoute().params;
        const uri = 'https://api.escuelajs.co/api/v1/products/' + id;

        // fetch the product 
        const {data: product} = await useFetch(uri, {key: id});
</script>

<style lang="scss" scoped>

</style>