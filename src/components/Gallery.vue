<template>
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
</template>

<script setup>
  import {ref} from "vue"
  const model = ref(null);

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

<style>

</style>