<template>
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
                            <div class="text-subtile-1 text-medium-emphasis">Destination</div>
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
</template>

<script setup>
    import {ref} from "vue"
    

    const tab = ref(null);
    
</script>

<style>

</style>