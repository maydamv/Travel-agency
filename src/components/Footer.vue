<template>
    <v-footer color="#FFFFFF" class="d-flex flex-column">
        <div class="d-flex w-100 px-6 pb-10 pt-8">

        </div>
        <div class="px-4 py-8 bgTop text-center w-100 text-black">
            <v-icon class="mr-2" color="black">mdi mdi-copyright</v-icon>
            <strong>
                >Copyright {{ new Date().getFullYear() }}. All Rights Reserved by MayMV
            </strong>
        </div>

    </v-footer>
</template>
    
<script setup>
    import {ref} from "vue"
    const hoteles = ref([
            {
                image: "/public/7.jpg"
            },
            {
                image: "/public/16.jpg"
            },
            {
                image: "/public/20.jpg"
            },
            {
                image: "/public/23.jpg"
            },
            {
                image: "/public/17.jpg"
            },
            {
                image: "/public/10.jpg"
            }
        ]);
</script>
    
<style scoped>
</style>