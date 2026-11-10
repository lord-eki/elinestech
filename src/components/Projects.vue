<script setup lang="ts">
import { ref } from 'vue';

const projects = ref([
    {
        category: 'Custom Software',
        title: 'Enterprise ERP & Logistics Platform',
        description: 'A scalable web system managing real-time inventory, dispatch tracking, and warehouse operations.',
        technologies: ['Next.js', 'TypeScript', 'PostgreSQL', 'Tailwind CSS'],
        extra: 2,
        sector: 'Supply Chain & Logistics'
    },
    {
        category: 'AI Solution',
        title: 'AI Document Intelligence & Extraction',
        description: 'Automated parsing, entity recognition, and validation pipeline processing complex financial and legal documents.',
        technologies: ['Python', 'FastAPI', 'PyTorch', 'Next.js'],
        extra: 2,
        sector: 'FinTech & Compliance'
    },
    {
        category: 'Mobile Application',
        title: 'PulseTrack Cross-Platform Clinical App',
        description: 'A mobile application connecting patients with healthcare specialists through encrypted video consultations.',
        technologies: ['React Native', 'TypeScript', 'WebRTC', 'Node.js'],
        extra: 2,
        sector: 'Healthcare'
    }
]);
</script>

<template>
    <div class="mt-16 grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 gap-8">

        <div v-for="project in projects" :key="project.title"
            class="border border-gray-200 rounded-xl overflow-hidden shadow-sm hover:shadow-lg transition duration-300">

            <div class="relative h-60 preview-pattern flex flex-col items-center justify-center gap-3">

                <span class="absolute top-3 right-3 bg-[#172943] text-white text-xs font-semibold px-3 py-1 rounded">
                    SAMPLE
                </span>

                <div class="w-12 h-12 rounded-xl bg-[#992B00] border border-[#087C89] flex items-center justify-center">
                    <svg xmlns="http://www.w3.org/2000/svg" class="w-6 h-6 text-teal-400" fill="none"
                        viewBox="0 0 24 24" stroke="currentColor" stroke-width="1.8">
                        <path stroke-linecap="round" stroke-linejoin="round" d="M8 9l-3 3 3 3m8-6l3 3-3 3m-3-8l-2 10" />
                    </svg>
                </div>

                <span class="text-gray-400 text-xs font-semibold tracking-widest uppercase">
                    {{ project.category }}
                </span>

            </div>

            <div class="p-6 grid gap-3">

                <div>
                    <span
                        class="bg-[#F5E0D7] text-[#992B00] border border-[#f4c9b8] rounded-md px-3 py-1 text-xs font-semibold">
                        {{ project.category }}
                    </span>
                </div>

                <h3 class="font-bold text-lg truncate">
                    {{ project.title }}
                </h3>

                <p class="text-gray-500 text-sm leading-relaxed line-clamp-3">
                    {{ project.description }}
                </p>

                <div class="flex flex-wrap gap-2">
                    <span v-for="technology in project.technologies" :key="technology"
                        class="text-xs border border-gray-200 rounded px-2 py-1">
                        {{ technology }}
                    </span>

                    <span v-if="project.extra" class="text-xs text-blue-500">
                        +{{ project.extra }}
                    </span>
                </div>

                <hr class="border-gray-200">

                <div class="flex justify-between items-center gap-2 text-sm">

                    <a href="#" class="font-semibold flex items-center gap-2 hover:text-[#992B00]">
                        View Project
                        <span>›</span>
                    </a>

                    <span class="text-xs text-gray-500 truncate">
                        {{ project.sector }}
                    </span>

                </div>

            </div>

        </div>

    </div>

    <div class="mt-16 flex justify-center mb-16">
        <button class=" flex items-center gap-4 rounded-xl pt-3 pb-3 pl-6 pr-6 border bg-[#992B00] text-white">
            <span>View All Projects</span>
            <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24">
                <title>arrow-right</title>
                <path fill="currentColor" d="M4 11v2h12l-5.5 5.5l1.42 1.42L19.84 12l-7.92-7.92L10.5 5.5L16 11z" />
            </svg> </button>
    </div>
</template>

<style scoped>
.preview-pattern {
    background-color: #0D1C36;
    background-image: radial-gradient(rgba(153, 43, 0, 0.45) 1px,
            transparent 1px);
    background-size: 16px 16px;
}
</style>
