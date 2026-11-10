<script setup lang='ts'>
import Logo from './icons/Logo.vue';

const navigation = [
    { label: 'Home', href: '/' },
    { label: 'Projects', href: '/projects' },
    { label: 'Services', href: '/services' },
    { label: 'About', href: '/about' },
    { label: 'Contact', href: '/contact' },
];

const services = [
    { label: 'Web Development', href: '/services/web-development' },
    { label: 'Mobile App Development', href: '/services/mobile-apps' },
    { label: 'AI Solutions', href: '/services/ai-solutions' },
    { label: 'Custom Software', href: '/services/custom-software' },
    { label: 'Automation', href: '/services/automation' },
];
</script>



<template>
    <footer class="relative overflow-hidden border-t border-slate-800 bg-[#0F1B30] text-slate-300">

        <div class="mx-auto max-w-7xl px-6 pb-8 pt-16 lg:px-10">

            <div class="grid grid-cols-1 gap-12 sm:grid-cols-2 lg:grid-cols-12 lg:gap-10">

                <div class="lg:col-span-5">

                    <a href="/" class="mb-7 inline-flex items-center gap-3">

                        <Logo />

                        <!-- <span class="text-2xl font-bold tracking-tight text-white">
                            E-linesTech
                        </span> -->

                    </a>


                    <p class="max-w-md text-sm leading-6 text-slate-300">
                        E-linesTech builds modern websites, web applications,
                        mobile apps, custom software, and AI-powered solutions
                        designed around real business needs.
                    </p>


                    <div class="mt-6 flex items-center gap-3">

                        <span class="relative flex h-2 w-2">
                            <span
                                class="absolute inline-flex h-full w-full animate-ping rounded-full bg-primary opacity-50"></span>
                            <span class="relative inline-flex h-2 w-2 rounded-full bg-primary"></span>
                        </span>

                        <span class="text-sm text-slate-400">
                            Available for new projects worldwide
                        </span>

                    </div>

                </div>


                <div class="lg:col-span-2">

                    <h3 class="mb-6 text-xs font-semibold uppercase tracking-wider text-slate-400">
                        Navigation
                    </h3>

                    <ul class="space-y-3">

                        <li v-for="item in navigation" :key="item.label">
                            <a :href="item.href"
                                class="text-sm text-slate-300 transition-colors duration-200 hover:text-[#D97745]">
                                {{ item.label }}
                            </a>
                        </li>

                    </ul>

                </div>


                <div class="lg:col-span-3">

                    <h3 class="mb-6 text-xs font-semibold uppercase tracking-wider text-slate-400">
                        Services
                    </h3>

                    <ul class="space-y-3">

                        <li v-for="item in services" :key="item.label">
                            <a :href="item.href"
                                class="text-sm text-slate-300 transition-colors duration-200 hover:text-[#D97745]">
                                {{ item.label }}
                            </a>
                        </li>

                    </ul>

                </div>


                <div class="lg:col-span-2">

                    <h3 class="mb-6 text-xs font-semibold uppercase tracking-wider text-slate-400">
                        Get in touch
                    </h3>

                    <div class="space-y-4">

                        <a href="mailto:hello@ledzora.com"
                            class="flex items-center gap-3 text-sm text-slate-300 transition-colors hover:text-[#D97745]">
                            <svg class="h-4 w-4 shrink-0 text-primary" viewBox="0 0 24 24" fill="none"
                                stroke="currentColor" stroke-width="1.8">
                                <rect x="3" y="5" width="18" height="14" rx="2" />
                                <path d="m3 7 9 6 9-6" />
                            </svg>

                            hello@elinestech.com
                        </a>


                        <div class="flex items-center gap-3 text-sm text-slate-400">

                            <svg class="h-4 w-4 shrink-0 text-primary" viewBox="0 0 24 24" fill="none"
                                stroke="currentColor" stroke-width="1.8">
                                <circle cx="12" cy="10" r="3" />
                                <path d="M19 10c0 5-7 12-7 12S5 15 5 10a7 7 0 1 1 14 0Z" />
                            </svg>

                            Kenya

                        </div>

                    </div>


                    <a href="/contact"
                        class="mt-8 inline-flex items-center gap-2 text-xs font-semibold text-[#D97745] transition-all hover:gap-3 hover:text-white">
                        Start a consultation

                        <span aria-hidden="true">→</span>
                    </a>

                </div>

            </div>


            <div class="my-12 border-t border-slate-800"></div>


            <div class="flex flex-col gap-5 pb-1 text-xs sm:flex-row sm:items-center sm:justify-between">

                <p class="text-slate-400">
                    © {{ new Date().getFullYear() }} ElinesTech. All rights reserved.
                    Professional software & AI technology services.
                </p>


                <div class="flex items-center gap-6">

                    <a href="/privacy-policy" class="text-slate-400 transition-colors hover:text-white">
                        Privacy Policy
                    </a>

                    <a href="/terms-and-conditions" class="text-slate-400 transition-colors hover:text-white">
                        Terms & Conditions
                    </a>

                </div>

            </div>

        </div>


        <a href="/contact"
            class="fixed bottom-5 right-6 z-50 inline-flex items-center gap-3 rounded-full border border-primary/70 bg-[#0F1B30] px-5 py-3 text-xs font-semibold text-white shadow-xl transition-all duration-300 hover:-translate-y-1 hover:bg-primary">

            <span class="relative">
                <svg class="h-4 w-4 text-[#D97745]" viewBox="0 0 24 24" fill="none" stroke="currentColor"
                    stroke-width="1.8">
                    <path
                        d="M21 11.5a8.4 8.4 0 0 1-.9 3.8 8.5 8.5 0 0 1-7.6 4.7 8.4 8.4 0 0 1-3.8-.9L3 21l1.9-5.7a8.4 8.4 0 0 1-.9-3.8A8.5 8.5 0 0 1 8.7 3.9a8.4 8.4 0 0 1 3.8-.9h.5a8.5 8.5 0 0 1 8 8v.5Z" />
                </svg>

                <span class="absolute -right-1 -top-1 h-2 w-2 rounded-full bg-primary"></span>
            </span>

            Ask the Architect

        </a>

    </footer>
</template>
