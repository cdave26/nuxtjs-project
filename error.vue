<template>
    <div class="mx-7 max-w-sm mx-auto text-center card">
        <p class="font-bold text-7x1 mt-7">
            {{ error.statusCode }}
        </p>
        <p class="font-bold text-6x1 mt-7">
            Ooops.
        </p>
        <p class="font-bold text-6x1 mt-7">
            {{ error.message }}
        </p>

        <button class="btn my-7" @click="handleClearError"> Go Home</button>
    </div>
</template>

<script setup>
import { handleError } from 'vue';

    defineProps(['error']);

    const handleClearError = () => clearError({redirect:'/'});
</script>

<style lang="scss" scoped>

</style>