<script setup lang="ts">
import { onMounted, ref } from 'vue';


const isDark = ref(false);

function applyTheme() {
    document.documentElement.classList.toggle('dark', isDark.value);
}

function toggleTheme(): void {
    isDark.value = !isDark.value;

    applyTheme();

    localStorage.setItem('theme', isDark.value ? 'dark' : 'light');

}


onMounted(() => {
    const savedTheme = localStorage.getItem('theme');

    if (savedTheme) {
        isDark.value = savedTheme === 'dark';
    } else {
        isDark.value = window.matchMedia('(prefers-color-scheme: dark)').matches;
    }

    applyTheme();
});

</script>


<template>
    <div class="flex gap-4 items-center">
        <button type="button" @click="" aria-label="isDark ? 'Switch to light mode' : 'Switch to dark mode'"
            title="isDark ? 'Switch to light mode' : 'Switch to dark mode'"
            class="w-9 h-9 rounded-xl flex items-center justify-center border border-gray-200 transition-all duration-200 cursor-pointer">
            <!-- Sun icon -->
            <svg v-if="!isDark" xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24"
                fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                class="text-amber-500">
                <circle cx="12" cy="12" r="4" />
                <path d="M12 2v2" />
                <path d="M12 20v2" />
                <path d="m4.93 4.93 1.41 1.41" />
                <path d="m17.66 17.66 1.41 1.41" />
                <path d="M2 12h2" />
                <path d="M20 12h2" />
                <path d="m6.34 17.66-1.41 1.41" />
                <path d="m19.07 4.93-1.41 1.41" />
            </svg>

            <!-- Moon icon -->
            <svg v-else xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none"
                stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"
                class="text-blue-400">
                <path
                    d="M20.985 12.486a9 9 0 1 1-9.473-9.472c.405-.022.617.463.402.807a6.5 6.5 0 0 0 8.268 8.268c.344-.215.829-.003.803.397" />
            </svg>
        </button>
        <button class="bg-[#992B00] rounded-xl px-3.5 py-1.5 text-white"> Start a Project </button>
    </div>

</template>