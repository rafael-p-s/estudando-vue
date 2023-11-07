<template>
    <div class="container mx-auto">
        <h1 class="text-lg font-bold">A empresa</h1>
        <NuxtLink :to="{ name: 'produtos-produto-a' }">Produto A</NuxtLink>
        <NuxtLink :to="{ name: 'produtos-produto-b' }">Produto B</NuxtLink>
        <br>
        <br>

    </div>
</template>

<!-- <script >
export default {
    data() {
        return {
            services: []
        }
    },
    
}
</script> -->
<script >
const { resolve } = require('path');

async function getPosts() {
    try {
        console.log('antes da conexão.');
        // Isso é uma PROMISE
        var response = await fetch('https://jsonplaceholder.typicode.com/users?_limited=3')
        //Quando ele finalizar de pegar a PROMISE, irá capturar irá vir para baixo e pegar o JSON.
        var posts = await response.json();
        console.log(posts);
        console.log('depois da conexão.');

    } catch (e) {
        console.log(e)
    }
}
getPosts();
</script>