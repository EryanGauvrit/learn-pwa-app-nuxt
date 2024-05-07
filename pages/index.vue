<template>
    <main class="container max-w-4xl m-auto">
        <h1 class="text-4xl text-center mt-8 uppercase font-bold">The Nuxt Shop</h1>
        <div class="flex justify-center space-x-4 mt-4">
            <button @click="filterData('burgers')" class="bg-primary text-background py-2 px-4 rounded-sm">Burgers</button>
            <button @click="filterData('desserts')" class="bg-primary text-background py-2 px-4 rounded-sm">Desserts</button>
            <button @click="filterData('drinks')" class="bg-primary text-background py-2 px-4 rounded-sm">Drinks</button>
        </div>
        <section class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 py-10">
            <ArticleCard v-for="item in data" :key="item.id" :article="item" />
        </section>
    </main>
</template>
<script setup>
    import burgers from '~/data/burgers.json';
    import desserts from '~/data/desserts.json';
    import drinks from '~/data/drinks.json';

    const data = ref([]);

    const filterData = (type) => {
        if (type === 'burgers') {
            data.value = burgers;
        } else if (type === 'desserts') {
            data.value = desserts;
        } else if (type === 'drinks') {
            data.value = drinks;
        }
    }

    onMounted(() => {
        data.value = burgers;
    });
</script>
