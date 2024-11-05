<script setup>
import jobData from "@/assets/jobs.json"
import { ref } from "vue";

let jobs = ref(jobData)
console.log("Jobs : ", jobs.value)
</script>

<template>
    <section class="bg-blue-50 px-4 py-10 grid grid-cols-1 md:grid-cols-3 gap-6">
        <div class="container-xl lg:container m-auto">
            <h2 class="text-3xl font-bold text-green-500 mb-3 text-center">
                Browse Jobs
            </h2>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
                <div v-for="job in jobs" :key="job.id">{{ job.title }}</div>
            </div>
        </div>
    </section>
</template>