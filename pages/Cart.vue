<template>
    <main class="container max-w-4xl m-auto mt-10">
        <div class="flex justify-between">
            <h1 class="text-2xl font-bold">Your cart</h1>
            <p class="text-xl font-bold">Total: {{ total }}€</p>
        </div>
        <section class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4 py-10">
            <div v-for="article in cart" :key="article.id" class="bg-card text-card-foreground border rounded-md shadow-sm hover:scale-[1.05] duration-200 overflow-hidden">
                <div class="flex justify-between p-4">
                    <h3 class="text-xl font-bold my-2">{{ article.name }}</h3>
                    <p class="text-xl font-bold mt-2">{{ article.price }}€</p>
                </div>
            </div>  
        </section>
    </main>

</template>

<script setup>
    const cart = useState('cart', () => []);

    const total = computed(() => {
        return cart.value.reduce((acc, article) => acc + article.price, 0);
    });
</script>