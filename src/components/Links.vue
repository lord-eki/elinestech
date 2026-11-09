<script setup lang="ts">
import { ref } from 'vue';


const links = ref([
    { label: 'Home', href: '/' },
    { label: 'Projects', href: '/projects' },
    { label: 'Services', href: '/services' },
    { label: 'About', href: '/about' },
    { label: 'Contact', href: '/contact' }
]);

</script>

<template>
    <nav class="flex items-center gap-6">
        <a v-for="link in links" :href="link.href" :key="link.href"
            class="text-black dark:text-white  hover:text-[#992B00] transition-colors">
            {{ link.label }}
        </a>
    </nav>
</template>