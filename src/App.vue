<template>
    <div id="app">
        <Brand/>
    </div>
</template>

<script>
    import Brand from './components/Brand.vue'

    export default {
        name: 'app',

        components: {
            Brand
        }
    }
</script>

<style>
    @tailwind base;
    @tailwind components;

    .btn {
        @apply inline-block px-5 py-3 rounded-lg text-sm uppercase tracking-wider font-semibold;
    }

    .btn:hover {
        @apply bg-blue-400;
    }

    .btn:focus {
        @apply outline-none shadow-outline;
    }

    .btn:active {
        @apply bg-blue-600
    }

    .btn-blue {
        @apply bg-blue-500 text-white 
    }

    .btn:hover {
        @apply bg-blue-400;
    }

    .btn:active {
        @apply bg-blue-600
    }

    .btn-gray {
        @apply bg-gray-400 text-gray-800 
    }

    .btn-gray:hover {
        @apply bg-gray-300;
    }

    .btn-gray:active {
        @apply bg-gray-600
    }

    @tailwind utilities;
</style>
