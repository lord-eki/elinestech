
<script setup lang="ts">

const props = defineProps({
        heading : String,
        description : String
    });

</script>


<template>
    <div class="text-center mt-16">
        <h2 class="text-3xl font-extrabold">{{props.heading}}</h2>
        <p class="text-lg text-gray-500  mt-3">
            {{ props.description }}
        </p>
    </div>
</template>