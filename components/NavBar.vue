<template>
    <div class="w-full px-[20%]">

        <div class="justify-between items-center py-6 flex">
            
            <div class="flex items-center">

                <svg xmlns="http://www.w3.org/2000/svg" fill="none" stroke="currentColor" stroke-width="2" class="w-6 h-6 mr-2" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25h-15a2.25 2.25 0 0 1-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75"/>
                </svg>

                <div>hello@cajerre.com</div>
            </div>

            <div class="flex">
                <div v-for="(social, key, index) in socials" :key="key" class="flex">
                    <a :href="social.url" target="_blank" class="text-text-primary">
                        {{ social.name }}
                    </a>
                    <div v-if="index != 2" class="mx-2">|</div>
                </div>
            </div>

        </div>

        <div class="h-1 bg-background-secondary rounded-full" />

    </div>
</template>

<script>
    export default {
        data(){
            return{
                socials: {
                    facebook: {
                        name: 'Facebook',
                        url: 'https://www.facebook.com/cajerre'
                    },
                    instagram: {
                        name: 'Instagram',
                        url: 'https://www.instagram.com/cajerre'
                    },
                    twitter: {
                        name: 'Twitter',
                        url: 'https://www.twitter.com/cajerre'
                    }
                }
            }
        }
    }
</script>