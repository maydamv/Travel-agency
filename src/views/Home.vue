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
.title1 {
    color: #1f3347;
    font-size:50px;
    font-style:bold;
}
.par1 {
    color:"AAA1B4";
    margin-left:100px;
}
.bt1 {
    margin-left: 100px;
}
.img1 {
    width: 100% !important;
    height: 100% !important;
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