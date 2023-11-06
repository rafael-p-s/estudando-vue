<template>
    <div>
        <div class="bg-gray-100">
            <div class="container mx-auto flex itens-center space-x-4 h-10 mb-10">
                <NuxtLink :to="{ name: 'a-empresa' }">A empresa</NuxtLink>
                <NuxtLink :to="{ name: 'servicos' }">Serviços</NuxtLink>
                <NuxtLink :to="{ name: 'produtos' }">Produtos</NuxtLink>
            </div>
        </div>
        <div class="container mx-auto">
            <Nuxt/>
        </div>
    </div>
</template>