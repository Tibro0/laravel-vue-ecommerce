<template>
    <div class="antialiased bg-gray-50 dark:bg-gray-900">
        <!-- Navbar Start -->
        <Navbar/>
        <!-- Navbar End -->

        <!-- Sidebar Start -->
        <Sidebar/>
        <!-- Sidebar End -->

        <!-- Main Content Start -->
        <slot/>
        <!-- Main Content End -->

    </div>
    </template>

    <script setup>
    import { onMounted } from 'vue'
    import { initFlowbite } from 'flowbite'
    import Navbar from './Navbar.vue';
    import Sidebar from './Sidebar.vue';

    // initialize components based on data attribute selectors
    onMounted(() => {
        initFlowbite();
    })
    </script>
