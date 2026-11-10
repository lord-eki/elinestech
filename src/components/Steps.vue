<script setup lang="ts">
const phases = [
    {
        number: '01',
        title: 'Discovery',
        label: 'PHASE 1',
        description: 'We learn about your business, goals, and the specific problem you need to solve.',
    },
    {
        number: '02',
        title: 'Strategy',
        label: 'PHASE 2',
        description: 'We define the scope, choose the right technologies, and create a clear development plan.',
    },
    {
        number: '03',
        title: 'Design',
        label: 'PHASE 3',
        description: 'We design the user experience and interface, ensuring it meets your brand and user expectations.',
    },
    {
        number: '04',
        title: 'Development',
        label: 'PHASE 4',
        description: 'We build your solution using modern, scalable technologies with clean architecture.',
    },
    {
        number: '05',
        title: 'Testing',
        label: 'PHASE 5',
        description: 'We rigorously test across devices and scenarios to ensure quality and reliability.',
    },
    {
        number: '06',
        title: 'Deployment',
        label: 'PHASE 6',
        description: 'We deploy your application to production with proper infrastructure and monitoring.',
    },
    {
        number: '07',
        title: 'Support',
        label: 'PHASE 7',
        description: 'We provide ongoing support, maintenance, and iterative improvements as your needs evolve.',
    },
    {
        number: '∞',
        title: 'Continuous Evolution',
        label: 'ONGOING',
        description: 'Post-deployment code maintenance, security patches, performance audits, and continuous iterative development as your customer base scales.',
        featured: true,
    },
];
</script>



<template>
    <section class="bg-slate-50 px-5 py-20">

        <div class="mx-auto max-w-6xl">

            <div class="mx-auto mb-12 max-w-2xl text-center">

                <span class="inline-flex items-center rounded-md
                    border border-primary/20 bg-primary-light
                    px-3 py-1 text-xs font-semibold text-primary">
                    How We Work
                </span>

                <h2 class="mt-4 text-2xl font-bold tracking-tight
                    text-slate-900 sm:text-3xl">
                    A Structured, Transparent Development Process
                </h2>

                <p class="mt-3 text-sm leading-6 text-slate-500 sm:text-base">
                    Every project follows an iterative, disciplined
                    methodology that guarantees code quality,
                    milestone predictability, and rapid communication.
                </p>

            </div>


            <div class="grid grid-cols-1 gap-4 sm:grid-cols-2 lg:grid-cols-4">

                <div v-for="phase in phases" :key="phase.number" class="rounded-xl border p-5 transition-all
                    duration-300 hover:-translate-y-1 hover:shadow-lg" :class="phase.featured
                        ? 'border-slate-900 bg-slate-900 text-white'
                        : 'border-slate-200 bg-white text-slate-900'">

                    <div class="mb-4 flex items-center justify-between">

                        <span class="text-sm font-bold" :class="phase.featured
                            ? 'text-primary-light'
                            : 'text-primary'">
                            {{ phase.number }}
                        </span>

                        <span class="rounded-sm border px-2 py-1
                            text-[9px] font-medium tracking-wide" :class="phase.featured
                                ? 'border-primary/40 bg-primary/20 text-orange-200'
                                : 'border-slate-200 bg-slate-50 text-slate-500'">
                            {{ phase.label }}
                        </span>

                    </div>


                    <h3 class="mb-2 text-sm font-bold">
                        {{ phase.title }}
                    </h3>

                    <p class="text-xs leading-5" :class="phase.featured
                        ? 'text-slate-300'
                        : 'text-slate-500'">
                        {{ phase.description }}
                    </p>

                </div>

            </div>

        </div>

    </section>
</template>
