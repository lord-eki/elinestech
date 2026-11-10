<script setup lang="ts">
import { ref } from 'vue';
import globe from '../assets/images/earth-globe-svgrepo-com.svg';
import mojo from '../assets/images/mojolicious-svgrepo-com.svg';
import database from '../assets/images/database-svgrepo-com.svg';
import mobile from '../assets/images/mobile-svgrepo-com.svg';

const services = ref([
    {
        label: 'Web Development',
        icon: globe,
        description: 'Business websites, web applications, SaaS platforms, dashboards, and custom portals built with modern frameworks.'
    },
    {
        label: 'Web Applications',
        icon: mojo,
        description: 'Business websites, web applications, SaaS platforms, dashboards, and custom portals built with modern frameworks.'
    },
    {
        label: 'API & Backend Development',
        icon: database,
        description: 'Robust API architectures, scalable backends, database design, microservices, and system integrations.'
    },
    {
        label: 'Mobile Apps',
        icon: mobile,
        description: 'Native iOS and Android apps, cross-platform mobile applications with seamless performance and user experience.'
    }
]);
</script>

<template>
    <div class="flex mt-12 justify-evenly gap-4 ">
        <div v-for="service in services"
            class=" transition ease-in-out delay-150 duration-300 hover:-translate-y-1 hover:scale-105 shadow-md inset-shadow grid gap-2 border rounded-xl border-gray-300 p-8 hover:border-[#992B00] hover:text-[#992B00]">
            <div class="flex pl-1 items-center bg-[#f4c9b8] rounded-xl w-12 h-12 mb-4  "><img :src="service.icon" class="w-10 h-10"/> </div>
            <div>{{ service.label }}</div>
            <div class="text-gray-400">{{ service.description }}</div>
            <hr class="text-gray-300">
            <div class="text-[#992B00] flex items-center gap-4">Learn more<svg xmlns="http://www.w3.org/2000/svg"
                    width="1em" height="1em" viewBox="0 0 24 24">
                    <title>arrow-right</title>
                    <path fill="currentColor" d="M4 11v2h12l-5.5 5.5l1.42 1.42L19.84 12l-7.92-7.92L10.5 5.5L16 11z" />
                </svg></div>
        </div>
    </div>
</template>