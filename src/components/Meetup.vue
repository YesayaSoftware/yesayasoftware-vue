<template>
    <div class="flex items-center rounded-lg bg-white shadow-lg overflow-hidden">
        <img :src="meetup.thumbnail" class="h-32 w-32 flex-shink-0 object-cover object-center" alt="Yesaya on Machine Learning Basics Meetup">

        <div class="px-6 py-4">
            <h3 class="text-lg font-semibold text-gray-800">
                {{ meetup.name }}
            </h3>

            <p class="text-gray-600">
                {{ meetup.description }}
            </p>

            <div class="mt-4">
                <a href="#" class="text-blue-500 hover:text-blue-400 active:text-blue-600 font-semibold">
                    Read more
                </a>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'Meetup',

        props: ['meetup'],
    }
</script>