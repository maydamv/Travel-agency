<template>
    <v-footer color="#FFFFFF" class="d-flex flex-column">
        <div class="d-flex w-100 px-6 pb-10 pt-8">
            <v-row>
                <v-col cols="12" sm="3">
                    <h4 class="mt-2">Explore</h4>
                    <span class="text-caption">
                        Continually productize<br />
                        compelling dome packed with<br />
                        all Elated utilize website and
                        <br />creating supply next-generation
                    </span>
                    <br />
                    <h4 class="mt-2">Follow Us On</h4>
                    <v-icon class="mr-1">mdi mdi-facebook</v-icon>
                    <v-icon class="mr-1">mdi mdi-twitter</v-icon>
                    <v-icon class="mr-1">mdi mdi-instagram</v-icon>
                    <v-icon class="mr-1">mdi mdi-whatsapp</v-icon>
                    <v-icon class="mr-1">mdi mdi-linkedin</v-icon>
                </v-col>
                <v-col cols="12" sm="3">
                    <h4 class="mt-2">Tour Type</h4>
                    <span class="text-caption">Adventure Tour</span><br />
                    <span class="text-caption">Group Tour</span><br />
                    <span class="text-caption">Seasonal Tour</span><br />
                    <span class="text-caption">Relaxation Tour</span><br />
                    <span class="text-caption">Family Friendly Tour</span><br />
                </v-col>
                <v-col cols="12" sm="3">
                    <h4 class="mt-2">Contact Info</h4>
                        <span class="text-caption">
                            <v-icon class="mr-1">mdi mdi-phone</v-icon> 
                            88130-589-745-6987<br />
                            +1655-456-523
                        </span><br />
                        <span class="text-caption">
                            <v-icon class="mr-1">mdi mdi-clock-time-eight</v-icon> 
                            Mon-Fri
                            09:00-18:00<br />
                            except public holidays
                        </span><br />
                        <span class="text-caption">
                            <v-icon class="mr-1">mdi mdi-map-marker</v-icon> 
                            25/2 Vokte
                            Street<br />
                            09:00-18:00<br />
                            Building Melborn City
                        </span><br />
                </v-col>
                <v-col cols="12" sm="3">
                    <h4 class="mt-2">Gallery</h4>
                    <v-row>
                        <v-col v-for="(hotel, i) in hoteles" :key="i" class="d-flex child-flex" cols="4">
                            <v-img 
                                :src="hotel.image"
                                aspect-ratio="1"
                                cover
                                class="bg-grey-lighten-2"
                            >
                            </v-img>
                        </v-col>
                    </v-row> 
                </v-col>

            </v-row>
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