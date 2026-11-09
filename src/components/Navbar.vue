<script setup lang="ts">
import Button from './Button.vue';
import Logo from './icons/Logo.vue';
import Links from './Links.vue';




</script>

<template>
    <nav class="w-full">
        <div class="mx-auto flex max-w-7xl items-center justify-between">
            <Logo />

            <Links />

            <Button />
        </div>
    </nav>
</template>