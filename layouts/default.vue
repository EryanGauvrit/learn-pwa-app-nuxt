<template>
    <div class="w-full bg-background text-foreground min-h-screen">
        <NuxtPwaManifest />
        <slot />
        <nav class="w-full flex justify-center bg-primary text-background items-center py-4 fixed bottom-0">
            <ul class="flex justify-around space-x-10">
                <li v-for="nav in navigations" :key="nav.name">
                    <NuxtLink :to="nav.path" class="hover:text-secondary px-4 py-1 rounded-sm font-bold ">
                        <Icon :name="nav.icon" class="w-10 h-10 inline" v-if="nav.icon" />
                    </NuxtLink>
                    
                </li>
            </ul>
        </nav>
    </div>
</template>

<script setup>

    const navigations = [
        { name: 'Menu', path: '/', icon: 'icon-park-outline:hamburger' },
        { name: 'Cart', path: '/cart', icon: 'mdi:basket-outline'},
        { name: 'Contact', path: '/contact', icon: 'material-symbols:contact-support-outline'},
    ]
</script>

<style scoped>
    .router-link-exact-active {
        @apply text-muted;    
    }
</style>