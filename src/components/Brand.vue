<template>
    <div>
        <div class="flex bg-gray-100">
            <div class="px-8 py-12 max-w-md mx-auto sm:max-w-xl lg:max-w-full lg:w-1/2 lg:py-24 lg:px-12">
                <div class="xl:max-w-lg xl:ml-auto">
                    <div class="flex items-center">
                        <img src="../assets/logo-rounded.svg" class="h-12" alt="Yesaya Software">

                        <h5 class="mx-4 text-2xl text-gray-700 font-semibold">
                            Yesaya <span class="text-blue-700">Software</span>
                        </h5>
                    </div>
                    

                    <img src="img/yesaya-presentation.jpg" class="mt-4 rounded-lg shadow-xl sm:mt-8 sm:h-72 sm:w-full sm:object-cover sm:object-center lg:hidden" alt="Yesaya on Presentation">
                
                    <h1 class="mt-6 text-2xl sm:mt-8 sm:text-4xl lg:text-3xl xl:text-4xl font-bold text-gray-900 leading-tight">
                        Sharing is caring. 
                        
                        <br class="hidden lg:inline">
                        <span class="text-blue-900">That's what Yesaya do.</span>
                    </h1>

                    <p class="mt-2 text-gray-600 sm:mt-4 sm:text-xl">
                        Yesaya is constantly participating in the local tech communities. 
                        He has been a speaker in a number of meetups.
                    </p>

                    <div class="mt-4 sm:mt-6">
                        <a href="#" class="btn btn-blue shadow-lg sm:text-base">
                            Listen the Podcast
                        </a>
                    </div>
                </div>
                
            </div>

            <div class="hidden lg:block lg:w-1/2 lg:relative">
                <img src="img/yesaya-presentation.jpg" class="absolute inset-0 h-full w-full object-cover object-center" alt="Yesaya on Presentation">
            </div>
        </div>

        <div>
            <div class="max-w-md sm:max-w-xl lg:max-w-6xl mx-auto px-8 lg:px-12 py-8">
                <h2 class="text-xl text-gray-900">Recent Event</h2>

                <p class="text-gray-600">
                    Events, meetups and conferences Yesaya attended recently.
                </p>

                <div class="flex flex-wrap -mx-4">
                    <div class="mt-6 w-full px-4 lg:w-1/2 xl:w-1/3" v-for="meetup in meetups" :key="meetup.id">
                        <Meetup :meetup="meetup" />
                    </div>
                </div>
            </div>
        </div>
    </div>
    
</template>

<script>
    import Meetup from '../components/Meetup.vue'

    export default {
        name: 'Brand',

        components: {
            Meetup
        },
        
        data() {
            return {
                meetups: [
                    {
                        id: 1,
                        name: "#KotlinEverywhere",
                        description: "Kotlin Basics",
                        thumbnail: "./img/yesaya-presentation.jpg"
                    },
                    {
                        id: 2,
                        name: "#DevFestDar",
                        description: "MVVM Architecture",
                        thumbnail: "./img/yesaya-devfest_iv.png"
                    },
                    {
                        id: 3,
                        name: "#MLBasics",
                        description: "Start ML with TF",
                        thumbnail: "./img/brand.jpg"
                    }
                ]
            }
        }
    }
</script>

<style scoped>
</style>
