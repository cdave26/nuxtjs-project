<template>
    <header class="shadow-sm bg-white p-5">
       <nav class="mx-auto flex justify-between">
        <NuxtLink to="/" class="font-bold">Nuxt Project</NuxtLink>
           <ul class="flex gap-4">
               <li> <NuxtLink to="/">Home</NuxtLink> </li>
               <li> <NuxtLink to="/about">About</NuxtLink> </li>
               <li> <NuxtLink to="/products">Products</NuxtLink> </li>
           </ul>
       </nav>
   </header>
<div class="container mx-auto p-4">
    <slot/>
</div>
</template>

<style scoped>
.router-link-exact-active{
    color: aquamarine;
}
</style>