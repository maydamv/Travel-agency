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
            
        </v-row>
    </v-container>
</v-main>


</template>

<script setup>
</script>

<style scoped>
</style>