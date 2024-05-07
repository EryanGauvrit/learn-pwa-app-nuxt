<template>
    <div class="bg-card text-card-foreground border rounded-md shadow-sm hover:scale-[1.05] duration-200 overflow-hidden">
        <NuxtImg v-if="article.img" :src="article.img" :alt="article.name" class="object-cover object-center h-36 w-full" />
        <span v-else class="bg-primary text-background text-2xl font-bold h-36 w-full flex items-center justify-center">No image</span>
        <div class="p-4">
            <div class="px-2">
                <h3 class="text-xl font-bold my-2">{{ article.name }}</h3>
                <p class="text-sm text-primary">{{ article.dsc }}</p>
                <p class="text-sm text-primary mt-2">Origin: {{ article.country }}</p>
            </div>
            <div class="flex justify-between">
                <p class="text-xl font-bold mt-2">rate : {{ article.rate }}/5</p>
                <p class="text-xl font-bold mt-2">{{ article.price }}€</p>
            </div>
            <div class="py-4">
                <button @click="addToCart(article)" class="w-full bg-primary text-background py-2 rounded-md">Add to cart</button>
            </div>
        </div>
    </div>

</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  article: Object,
});

const cart = useState('cart', () => []);

const addToCart = (article) => {
    cart.value.push(article);
};
</script>