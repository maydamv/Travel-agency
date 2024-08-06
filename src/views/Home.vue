<template>

<Navbar/>
<v-main>
    <v-container>
        <v-row>
            <v-col cols="12">
                <v-row>
                    <v-col cols="12" sm="6">
                        <h1 class="title1">
                            It's a Big World <br/>
                            Out There, Go <br/>
                            Explore
                        </h1>
                        <p class="par1">
                            Conveniently customiz proactiv web service for <br/>
                                leveraged without continualliery aggregate fricctionle
                                <br/>ou wellies richard, and very customize continually.
                        </p>
                        <v-btn class="text-noe nt-8 bt1" color="indigo-lighten-1" size="x-large" variant="flat" rounded="0">
                            Get Exploration
                        </v-btn>
                        <v-btn class="text-none ml-2 text-indigo-lighten-1 mt-8" size="x-large" variant="flat" rounded="0">
                            Read More
                        </v-btn>
                    </v-col>
                    <v-col cols="12" sm="6">
                        <v-img src="/public/2.jpg" class="img1"></v-img>
                    </v-col>
                </v-row>
            </v-col>
            <v-col cols="12" sm="12">
                <v-card flat>
                    <v-tabs v-model="tab" color="indigo-lighten-1" align-tabs="center">
                        <v-tab :value="1">
                            <v-icon class="mr-2">mdi mdi-bed</v-icon>Hotel
                        </v-tab>
                        <v-tab :value="2">
                            <v-icon class="mr-2">mdi mdi-airplane-takeoff</v-icon>Flight
                        </v-tab>
                        <v-tab :value="3">
                            <v-icon class="mr-2">mdi mdi-car</v-icon>Car
                        </v-tab>
                        <v-tab :value="4">
                            <v-icon class="mr-2">mdi mdi-ferry</v-icon>Ship
                        </v-tab>
                    </v-tabs>
                    <v-window v-model="tab">
                        <v-window-item v-for="n in 4" :key="n" :value="n">
                            <v-container fluid>
                                <v-row>
                                    <v-col cols="12" sm="2">
                                        <div class="text-subtile-1 text-medium-emphasis">Your Destination</div>
                                        <v-select density="compact" placeholder="Destination" :items="[
                                            'California',
                                            'Colorado',
                                            'Florida',
                                            'Georgia',
                                            'Texas',
                                            'Wyoming',
                                        ]"
                                         variant="outlined"></v-select>
                                    </v-col>
                                    <v-col cols="12" sm="2">
                                        <div class="text-subtile-1 text-medium-emphasis">Check in</div>
                                        <v-text-field density="compact" placeholder="Date" type="date" variant="outlined"></v-text-field>
                                    </v-col>
                                    <v-col cols="12" sm="2">
                                        <div class="text-subtile-1 text-medium-emphasis">Check out</div>
                                        <v-text-field density="compact" placeholder="Date" type="date" variant="outlined"></v-text-field>
                                    </v-col>
                                    <v-col cols="12" sm="2">
                                        <div class="text-subtile-1 text-medium-emphasis">Child</div>
                                        <v-select density="compact" placeholder="Child" :items="[
                                            '0',
                                            '1',
                                            '2',
                                            '3',
                                            '4',
                                            '5',
                                        ]"
                                         variant="outlined"></v-select>
                                    </v-col>
                                    <v-col cols="12" sm="2">
                                        <div class="text-subtile-1 text-medium-emphasis">Adult</div>
                                        <v-select density="compact" placeholder="Adult" :items="[
                                            '1',
                                            '2',
                                            '3',
                                            '4',
                                            '5',
                                            '6',
                                        ]"
                                         variant="outlined"></v-select>
                                    </v-col>
                                    <v-col cols="12" sm="2">
                                        <v-btn class="text-none mt-5" color="indigo-lighten-1" size="x-large" variant="flat" rounded="0" elevation="12">
                                            Book Now
                                        </v-btn>
                                    </v-col>
                                </v-row>
                            </v-container>
                        </v-window-item>
                    </v-window>
                </v-card>
            </v-col>
            <v-col cols="12">
                <v-col>
                    <h4 class="text-center text-indigo-lighten-1">Featured Tours</h4>
                    <h1 class="text-center">Beautiful Places Around The World</h1>
                </v-col>
                <v-row justify="center">
                    <v-col cols="12" sm="10">
                        <v-row>
                            <v-col cols="12" sm="4">
                                <v-hover v-slot="{ isHovering, props}">
                                <v-card :elevation="isHovering ? 12: 2" :class="{ 'on-hover':isHovering }" v-bind="props" class="card1">
                                    <v-img src="/public/4.png" cover height="100%">
                                        <div class="d-flex flex-row-reverse">
                                            <v-btn class="text-none mr-2 mt-2" color="indigo-lighten-1" size="x-large" variant="flat" rounded="0" elevation="12">
                                                3 Packages
                                            </v-btn>
                                        </div>
                                        <div class="text-white top">
                                            <h1 class="mt-4">Paris</h1>
                                            <div>
                                                <p class="ma-0 text-body-1 font-weight-bold">
                                                    Starting From $1200
                                                </p>
                                            </div>
                                        </div>
                                        <div class="d-flex justify-center">
                                            <v-btn v-for="(icon, index) in icons" :key="index" variant="text" :class="{ 'show-btns' : isHovering}" :color="transparent" :icon="icon"></v-btn>
                                        </div>
                                    </v-img>
                                </v-card>  
                                </v-hover>
                            </v-col>
                            <v-col cols="4" class="d-flex flex-column">
                                <v-row>
                                    <v-col cols="12">
                                        <v-hover v-slot="{ isHovering, props}">
                                            <v-card :elevation="isHovering ? 12: 2" :class="{ 'on-hover':isHovering }" v-bind="props" class="card1">
                                                <v-img src="/public/5.jpg" cover height="100%">
                                                    <div class="d-flex flex-row-reverse">
                                                        <v-btn class="text-none mr-2 mt-2" color="indigo-lighten-1" size="x-large" variant="flat" rounded="0" elevation="12">
                                                            3 Packages
                                                        </v-btn>
                                                    </div>
                                                    <div class="text-white ">
                                                        <h1 class="mt-10 ml-4">Brazil</h1>
                                                        <div>
                                                            <p class="ma-0 text-body-1 font-weight-bold ml-4">
                                                                Starting From $1900
                                                            </p>
                                                        </div>
                                                    </div>
                                                    <div class="d-flex justify-center">
                                                        <v-btn v-for="(icon, index) in icons" :key="index" variant="text" :class="{ 'show-btns' : isHovering}" :color="transparent" :icon="icon"></v-btn>
                                                    </div>
                                                </v-img>
                                            </v-card>  
                                        </v-hover>
                                    </v-col>
                                    <v-col cols="12">
                                        <v-hover v-slot="{ isHovering, props}">
                                            <v-card :elevation="isHovering ? 12: 2" :class="{ 'on-hover':isHovering }" v-bind="props" class="card1">
                                                <v-img src="/public/13.jpg" cover height="100%">
                                                    <div class="d-flex flex-row-reverse">
                                                        <v-btn class="text-none mr-2 mt-2" color="indigo-lighten-1" size="x-large" variant="flat" rounded="0" elevation="12">
                                                            3 Packages
                                                        </v-btn>
                                                    </div>
                                                    <div class="text-white ">
                                                        <h1 class="mt-10 ml-4">Japon</h1>
                                                        <div>
                                                            <p class="ma-0 text-body-1 font-weight-bold ml-4">
                                                                Starting From $1500
                                                            </p>
                                                        </div>
                                                    </div>
                                                    <div class="d-flex justify-center">
                                                        <v-btn v-for="(icon, index) in icons" :key="index" variant="text" :class="{ 'show-btns' : isHovering}" :color="transparent" :icon="icon"></v-btn>
                                                    </div>
                                                </v-img>
                                            </v-card>  
                                        </v-hover>
                                    </v-col>
                                </v-row>
                            </v-col>
                            <v-col cols="12" sm="4">
                                <v-hover v-slot="{ isHovering, props}">
                                <v-card :elevation="isHovering ? 12: 2" :class="{ 'on-hover':isHovering }" v-bind="props" class="card1">
                                    <v-img src="/public/9.jpg" cover height="100%">
                                        <div class="d-flex flex-row-reverse">
                                            <v-btn class="text-none mr-2 mt-2" color="indigo-lighten-1" size="x-large" variant="flat" rounded="0" elevation="12">
                                                3 Packages
                                            </v-btn>
                                        </div>
                                        <div class="text-white top">
                                            <h1 class="mt-4">London</h1>
                                            <div>
                                                <p class="ma-0 text-body-1 font-weight-bold">
                                                    Starting From $1200
                                                </p>
                                            </div>
                                        </div>
                                        <div class="d-flex justify-center">
                                            <v-btn v-for="(icon, index) in icons" :key="index" variant="text" :class="{ 'show-btns' : isHovering}" :color="transparent" :icon="icon"></v-btn>
                                        </div>
                                    </v-img>
                                </v-card>  
                                </v-hover>
                            </v-col> 
                        </v-row>
                    </v-col>
                </v-row>
            </v-col>

            <v-col cols="12" sm="12">
                <h4 class="text-center text-indigo-lighten-1">Popular Packeg</h4>
                <h1 class="text-center">Checkout Our Packages</h1>
                <v-row justify="center">
                    <v-col cols="12" sm="10">
                        <v-row>
                            <v-col cols="12" sm="3" v-for="(popular,i) in populars" :key="i">
                                <v-hover v-slot="{isHovering, props}">
                                    <v-card class="mx-auto" color="grey-lighten-4" max-width="600" v-bind="props">
                                        <v-img :aspect-ratio="16 /9" cover :src="popular.image">
                                            <v-expand-transition>
                                                <div v-if="isHovering" class="d-flex transition-fast-in-fast-out bg-red-lighten-1 v-card--reveal" style="height: 100%">
                                                    <v-row>
                                                        <v-col cols="12" sm="12">
                                                            <h1 class="ml-4">{{ popular.subtitle1 }}</h1>
                                                        </v-col>
                                                        <v-col cols="12" sm="12">
                                                            <h6 class="ml-4 mt-n4 mb-3">{{ popular.subtitle2 }}</h6>
                                                        </v-col>
                                                    </v-row>
                                                </div>
                                            </v-expand-transition>
                                        </v-img>
                                        <v-card-text class="pt-6">
                                            <div class="font-weight-light text-grey text-h6 mb-2">
                                                {{ popular.title }}
                                            </div>
                                        </v-card-text>
                                        <v-card-actions>
                                            <span class="text-grey-darken-2 text-caption me-2">
                                                ({{ rating }})
                                            </span>
                                            <v-rating v-model="rating" color="white" active-color="yellow-accent-4" half-increments hover size="18"></v-rating>  
                                            <v-spacer></v-spacer>
                                            <v-btn class="text-none" color="indigo-lighten-1" size="large" variant="flat" rounded="0" elevation="6">{{ popular.money }}</v-btn>
                                        </v-card-actions>
                                    </v-card>
                                </v-hover>
                            </v-col>
                        </v-row>
                    </v-col>
                </v-row>
            </v-col>

            <v-col cols="12" sm="12">
                <h4 class="text-center text-indigo-lighten-1">Inventore Varitatis</h4>
                <h1 class="text-center">Select Offres For Travelings</h1>
                <v-row justify="center">
                    <v-col cols="12" sm="10">
                        <v-row>
                            <v-col cols="12" sm="2" v-for="(offer,i) in offers" :key="i">
                                <v-card class="mx-auto px-2 pt-6" height="200px" flat>
                                    <div align="center" justify="center">
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
            </v-col>

            <v-col>    
                <h4 class="text-center text-indigo-lighten-1">Popular Hotel</h4>
                <h1 class="text-center">Most Popular Hotel</h1>
                <v-row justify="center">
                    <v-col cols="12" sm="10">
                       <v-row>
                            <v-col cols="12" sm="3" v-for="(hotel, i) in hotels" :key="i">
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
            </v-col>

            <v-col cols="12" sm="12">
                <h4 class="text-center text-indigo-lighten-1">Our Gallery</h4>
                <h1 class="text-center">Best Traveler Share a photo</h1>
                <v-sheet class="mx-auto" elevation="0" max-width="1200">
                    <v-slide-group v-model="model" class="pa-4" center-active show-arrows>
                        <v-slide-group-item v-for="travel in travels" :key="travel" v-slot="{isSelected, toggle}">
                            <v-card :color="isSelected ? 'primary' : 'grey-lighten-1'" class="ma-4" height="200" width="130" @click="toggle">
                                <div class="d-flex fill-height align-center justify-center">
                                    <v-img :src="travel.image" cover height="100%" width="100%"></v-img>
                                </div>
                            </v-card>
                        </v-slide-group-item>
                    </v-slide-group>
                </v-sheet>
            </v-col>
            <v-col cols="12" sm="12">
               <v-card>
                    <v-img src="/IMG-20240725-WA0075.jpg" cover height="100%">
                        <div class="d-flex justify-center ligne1">
                            <h1>Sign up for our newsletter</h1>
                        </div>
                        <div class="d-flex justify-center ligne2">
                            <v-text-field density="compact" placeholder="Enter your e-mail here" variant="solo-inverted" color="#393E50" rounded="0"></v-text-field>
                            <v-btn class="text-none tp" color="indigo-lighten-1" size="large" variant="flat" rounded="0" elevation="12">
                                Subscribe Now
                            </v-btn>
                        </div>
                    </v-img>
               </v-card> 
            </v-col>
        </v-row>
    </v-container>
</v-main>
<Footer_my/>

</template>

<script setup>
    import Navbar from "@/components/Navbar.vue"
    import {ref} from "vue"
    import Footer_my from "@/components/Footer_my.vue";

    const tab = ref(null);
    const model = ref(null);
    const icons = ref(["mdi-rewind","mdi-play", "mdi-fast-forward"]);
    const transparent = "rgba(255, 255, 255, 0)"
    const rating = ref(4.5);
    
    const populars = ref([
        {
            image: "/public/19.jpg",
            title: "Enjoy The Beauty Place in Greece City",
            subtitle1: "Grece",
            subtitle2: "4 Day's 3 Night",
            money: "$1200"
        },
        {
            image: "/public/14.jpg",
            title: "Enjoy The Beauty Place in Paris City",
            subtitle1: "Paris",
            subtitle2: "4 Day's 3 Night",
            money: "$1700"
        },
        {
            image: "/public/18.jpg",
            title: "Enjoy The Beauty Place in Bhutan City",
            subtitle1: "Bhutan",
            subtitle2: "3 Day's 2 Night",
            money: "$900"
        },
        {
            image: "/public/23.jpg",
            title: "Enjoy The Place in Maldivs Beach",
            subtitle1: "Maldivs",
            subtitle2: "5 Day's 4 Night",
            money: "$1300"
        },
    ]);

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
    const travels = ref([
        {
            image: "/public/a.jpg"
        },
        {
            image: "/public/b.jpg"
        },
        {
            image: "/public/c.jpg"
        },
        {
            image: "/public/d.jpg"
        },
        {
            image: "/public/e.jpg"
        },
        {
            image: "/public/f.jpg"
        },
        {
            image: "/public/g.jpg"
        },
        {
            image: "/public/h.jpg"
        },
        {
            image: "/public/i.jpg"
        },
        {
            image: "/public/j.jpg"
        },
        {
            image: "/public/k.jpg"
        },
        {
            image: "/public/l.jpg"
        }
    ]);
</script>

<style scoped>
.title1 {
    color: #1f3347;
    font-size:50px;
    font-style:bold;
    margin-left: 100px;
    margin-top:70px;
}
.par1 {
    color:"AAA1B4";
    margin-left:100px;
}
.bt1 {
    margin-left: 100px;
}
.img1 {
    width: 1000px !important;
    height: 1000px !important;
    z-index: 1;
    margin-top: -200px;
}
.v-card.card1 {
    transition: opacity 0.4s ease-in-out;
}
.v-card-card1:not(.on-hover) {
    opacity: 0.6;
}
.show-btns {
    color:rgba(255, 255, 255, 1) !important;
}
.top{
    margin-top:100%;
    margin-left: 20px;
}
.v-card--reveal {
    align-items: end;
    bottom: 0;
    justify-content: start;
    opacity: 0.9;
    position: absolute;
    width: 100%;
}
</style>