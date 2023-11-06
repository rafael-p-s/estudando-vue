<template>
    <div class="container mx-auto">
        <h1 class="text-lg font-bold">A empresa</h1>
        <NuxtLink :to="{ name: 'produtos-produto-a' }">Produto A</NuxtLink>
        <NuxtLink :to="{ name: 'produtos-produto-b' }">Produto B</NuxtLink>
        <br>
        <br>
        <pre>
                    {{ $fetchState }}
                </pre>
        <div v-if="$fetchState.pending">
            Carregando ...
        </div>
        <div v-else>
            <div v-for="service in services" :key="service.id" class="border-b border-gray-400 py-4">
                {{ service.usernamee }}
            </div>
        </div>
    </div>
</template>
<script>

export default {
    data() {
        return {
            services: []
        };
    },

    async fetch() {
        this.services = await this.$axios.$get('https://jsonplaceholder.typicode.com/users?_limit=2')
    },

}
</script>
