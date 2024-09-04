<template>
<Navbar/>
<div>
    <v-container>
        <v-row>
            <v-col cols="12">
                <Presentation/>   
            </v-col>
            <v-col cols="12" sm="12">
                <Reservation/>
            </v-col>
            <v-col cols="12">
                <Places/>
            </v-col>
            <v-col cols="12" sm="12">
                <Popular_Packages/>
            </v-col>
            <v-col cols="12" sm="12">
                <Offers/>
            </v-col>
            <v-col>    
                <Hotel/>
            </v-col>
            <v-col cols="12" sm="12">
                <Gallery/>
            </v-col>
            <v-col cols="12" sm="12">
               <Suscribe/>
            </v-col>
        </v-row>
    </v-container>
</div>
<Footer_my/>
</template>

<script setup>
    import Navbar from "@/components/Navbar.vue"
    import Footer_my from "@/components/Footer_my.vue";
    import Presentation from "@/components/Presentation.vue";
    import Reservation from "@/components/Reservation.vue";
    import Places from "@/components/Places.vue";
    import Popular_Packages from "@/components/Popular_Packages.vue";
    import Offers from "@/components/Offers.vue";
    import Hotel from "@/components/Hotel.vue";
    import Gallery from "@/components/Gallery.vue";
    import Suscribe from "@/components/Suscribe.vue";
</script>

<style scoped>
</style>