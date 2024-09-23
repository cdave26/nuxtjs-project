<template>
 <header class="shadow-sm bg-white p-5">
       <nav class="mx-auto flex justify-between">
        <NuxtLink to="/" class="font-bold">Nuxt Project</NuxtLink>
        </nav>
 </header>
<div class="container mx-auto p-4">
    <slot/>
</div>
<footer class="container mx-auto p-4 flex justify-between border-t-2">
    <nav>
        <ul class="flex gap-4">
            <li> <NuxtLink to="/">Home</NuxtLink> </li>
            <li> <NuxtLink to="/about">About</NuxtLink> </li>
            <li> <NuxtLink to="/products">Products</NuxtLink> </li>
        </ul>
    </nav>  
</footer>
</template>

<style scoped>
.dave .router-link-exact-active{
    color: rgb(180, 127, 255);
}
</style>