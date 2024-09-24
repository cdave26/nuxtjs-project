<template>
    <div class="card">
        <div class="grid grid-cols-2 gap-10">
            <div class="p-7">
                <img :src="product.category.image" alt="" class="mx-auto my-7">
            </div>
            <div>
                 <div class="p-7">
                    <h2 class="text-4x1 my-7">{{ product.title }}</h2>
                    <p>Price - $ {{ product.price  }}</p>
                    <h3>product description:</h3>
                    <p>{{ product.description }}</p>
                 </div>
            </div>
        </div>
    </div>
</template>

<script setup>
    const { product }  = defineProps(['product'])
</script>

<style scoped>
    .img  {
        max-width: 400px;
    }

</style>