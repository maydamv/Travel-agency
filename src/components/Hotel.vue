<template>
      <h4 class="text-center text-indigo-lighten-1">Popular Hotel</h4>
                <h1 class="text-center">Most Popular Hotel</h1>
                <v-row justify="center">
                    <v-col cols="12" sm="10">
                       <v-row class="d-flex justify-center">
                            <v-col cols="12" lg="3" md="4" sm="6" v-for="(hotel, i) in hotels" :key="i">
                                <v-hover v-slot="{isHovering, props}">
                                    <v-card class="mx-auto" color="grey-lighten-4" max-width="600" v-bind="props">
                                        <v-img :aspect-ratio="16 /9" cover :src="hotel.image">
                                            <v-expand-transition>
                                                <div v-if="isHovering" class="d-flex transition-fast-in-fast-out bg-teal-lighten-1 v-card--reveal" style="height: 100%">
                                                    <v-row>
                                                        <v-col cols="12" sm="12">
                                                            <h1 class="ml-4">{{ hotel.subtitle1 }}</h1>
                                                        </v-col>
                                                        <v-col cols="12" sm="12">
                                                            <h6 class="ml-4 mt-n4 mb-3">{{ hotel.subtitle2 }}</h6>
                                                        </v-col>
                                                    </v-row>
                                                </div>
                                            </v-expand-transition>
                                        </v-img>
                                        <v-card-text class="pt-6">
                                            <div class="font-weight-light text-grey text-h6 mb-2">
                                                {{ hotel.title }}
                                            </div>
                                            <div class="font-weight-light text-caption">
                                                <v-icon color="indigo-lighten-1">
                                                    mdi mdi-map-marker
                                                </v-icon> Bali, Indonesha
                                            </div>
                                        </v-card-text>
                                        <v-card-actions>
                                            <span class="text-grey-darken-2 text-caption me-2">({{ rating }})</span>
                                            <v-rating v-model="rating" color="white" active-color="yellow-accent-4" half-increments hover size="18"></v-rating>  
                                            <v-spacer></v-spacer>
                                            <v-btn class="text-none" color="indigo-lighten-1" size="large" variant="flat" rounded="0" elevation="6">{{ hotel.money }}</v-btn>
                                        </v-card-actions>
                                    </v-card>
                                </v-hover>                                         
                            </v-col>     
                       </v-row> 
                    </v-col>
                </v-row>
</template>

<script setup>
    import {ref} from "vue"
    const rating = ref(4.5);
    
    const hotels = ref([
        {
            image: "/public/grece.jpg",
            title: "Enjoy The Beauty Place in Greece City",
            subtitle1: "Grece",
            subtitle2: "4 Day's 3 Night",
            money: "$1200"
        },
        {
            image: "/public/paris.jpg",
            title: "Enjoy The Beauty Place in Paris City",
            subtitle1: "Paris",
            subtitle2: "4 Day's 3 Night",
            money: "$1700"
        },
        {
            image: "/public/maldivs.jpg",
            title: "Enjoy The Place in Maldivs Beach",
            subtitle1: "Maldivs",
            subtitle2: "5 Day's 4 Night",
            money: "$1300"
        },
        {
            image: "/public/bhutan.jpg",
            title: "Enjoy The Beauty Place in Bhutan City",
            subtitle1: "Bhutan",
            subtitle2: "3 Day's 2 Night",
            money: "$900"
        },
        
    ]);
    
</script>

<style>

</style>