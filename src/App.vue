<script setup>
import TheHeader from '@/components/TheHeader.vue'
import Stack from "@/components/Stack.vue";
import Project from "@/components/Project.vue";
</script>

<template>
    <TheHeader/>
    <div class="content">
        <Project/>
        <Stack/>
    </div>

    <footer>
        This website was made with ❤️ by me using Vue.js. It is hosted on Netlify.
    </footer>
</template>

<style scoped>

footer {
    text-align: center;
    font-size: 20px;
    padding: 15px;
}
</style>
