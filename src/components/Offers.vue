<template>
    <h4 class="text-center text-indigo-lighten-1">Inventore Varitatis</h4>
                <h1 class="text-center">Select Offers For Travelings</h1>
                <v-row justify="center">
                    <v-col cols="12" sm="10">
                        <v-row>
                            <v-col cols="12" sm="2" v-for="(offer,i) in offers" :key="i">
                                <v-card class="mx-auto px-2 pt-6" height="200px" flat>
                                    <div class="align-center justify-center">
                                        <v-img :src="offer.image" height="100px" width="100px"></v-img>       
                                    </div>
                                    <v-card-title class="text-center">
                                        <h6>{{ offer.title }}</h6>
                                    </v-card-title>
                                </v-card>
                            </v-col>
                        </v-row>
                    </v-col>
                </v-row>
</template>

<script setup>
    import {ref} from "vue"
    
    
    const offers = ref([
        {
            image: "/public/torre.jpg",
            title: "Different Countries",
        },
        {
            image: "/public/bus.jpg",
            title: "Bus Tours",
        },
        {
            image: "/public/food2.jpg",
            title: "Food Tours"
        },
        {
            image: "/public/summer.jpg",
            title: "Summer Rest"
        },
        {
            image: "/public/ship.jpg",
            title: "Ship Cruises"
        },
        {
            image: "/public/mountain.jpg",
            title: "Mountains Tours"
        }
    ]);

</script>

<style>

</style>