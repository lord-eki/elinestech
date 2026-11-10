<script setup lang="ts">
import { onMounted, onUnmounted, ref } from 'vue';


const applications = [
    'Mobile Applications',
    'Web Applications'
];

const currentIndex = ref(0);

let rotationTimer: ReturnType<typeof setInterval>;

onMounted(() => {
    rotationTimer = setInterval(() => {
        currentIndex.value = (currentIndex.value + 1) % applications.length;
    }, 2500);
});

onUnmounted(() => {
    clearInterval(rotationTimer);
});

</script>


<template>
    <div class="flex justify-between pt-6 items-center">
        <div>
            <h1 class="text-5xl font-bold leading-tight">
                Crafting
            </h1>

            <h1 class="text-5xl font-bold leading-tight">
                <Transition name="text-rotate" mode="out-in">
                    <span :key="currentIndex" class="text-[#992B00] inline-block">
                        {{ applications[currentIndex] }}
                    </span>
                </Transition>
            </h1>

            <h1 class="text-5xl font-bold leading-tight">
                Solutions
            </h1>
            <p class="text-gray-400 text-lg pt-4">We specialise in building web applications , mobile applications ,
                <br> websites and AI solutions bearing in mind the best industry standards in terms of
                security,scalability and reliability.
            </p>

            <div class="flex gap-8 pt-8">
                <button class=" flex items-center gap-4 rounded-xl pt-3 pb-3 pl-6 pr-6 border bg-[#992B00] text-white">
                    <span>Start a Project</span>
                    <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24">
                        <title>arrow-right</title>
                        <path fill="currentColor"
                            d="M4 11v2h12l-5.5 5.5l1.42 1.42L19.84 12l-7.92-7.92L10.5 5.5L16 11z" />
                    </svg> </button>
                <button
                    class=" flex gap-4 items-center rounded-xl pt-3 pb-3 pl-6 pr-6  border border-gray-200 hover:border-[#992B00]">
                    <span>View our Work</span>
                    <svg xmlns="http://www.w3.org/2000/svg" width="1em" height="1em" viewBox="0 0 24 24">
                        <title>arrow-top-right-thin</title>
                        <path fill="currentColor" d="m11.93 5l2.83 2.83L5 17.59L6.42 19l9.76-9.75L19 12.07V5z" />
                    </svg>
                </button>
            </div>
        </div>
        <div>
            <img src="../assets/images/hero_phone.svg" class="pr-8">
        </div>
    </div>


</template>