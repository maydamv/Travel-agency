<template>
    <v-app-bar>
        <div class="d-flex align-center" style="width: 200px; padding: 20px;">
            <v-img src="/public/11.jpg"></v-img>
            <v-app-bar-title>Explore</v-app-bar-title>
        </div>
        <v-spacer></v-spacer>
        <div class="d-none d-md-block">
            <v-menu transition="slide-x-transition">
                <template v-slot:activator="{props}">
                    <v-btn color="#6347F9" v-bind="props">Home +</v-btn>
                </template>
                <v-list>
                    <v-list-item>
                        <v-list-item-title>Home page one</v-list-item-title>
                        <v-list-item-title>Home page two</v-list-item-title>
                    </v-list-item>
                </v-list> 
            </v-menu>
            <v-menu transition="slide-x-transition">
                <template v-slot:activator="{props}">
                    <v-btn color="#6347F9" v-bind="props">Tours +</v-btn>
                </template>
                <v-list>
                    <v-list-item>
                        <v-list-item-title>Tour Grid</v-list-item-title>
                        <v-list-item-title>Tour List</v-list-item-title>
                        <v-list-item-title>Tour Single</v-list-item-title>
                    </v-list-item>
                </v-list>   
            </v-menu>
            <v-menu transition="slide-x-transition">
                <template v-slot:activator="{props}">
                    <v-btn color="#6347F9" v-bind="props">Hotel </v-btn>
                </template>
            </v-menu>
            <v-menu transition="slide-x-transition">
                <template v-slot:activator="{props}">
                    <v-btn color="#6347F9" v-bind="props">Pages +</v-btn>
                </template>
                <v-list>
                    <v-list-item>
                        <v-list-item-title>About</v-list-item-title>
                        <v-list-item-title>Team</v-list-item-title>
                        <v-list-item-title>Faq</v-list-item-title>
                        <v-list-item-title>404</v-list-item-title>                
                    </v-list-item>
                </v-list>
            </v-menu>
            <v-menu transition="slide-x-transition">
                <template v-slot:activator="{props}">
                    <v-btn color="#6347F9" v-bind="props">Blog </v-btn>
                </template>
            </v-menu>
            <v-menu transition="slide-x-transition">
                <template v-slot:activator="{props}">
                    <v-btn color="#6347F9" v-bind="props">Contact </v-btn>
                </template>
            </v-menu>
            <v-btn class="text-none expl mr-8" color="indigo-lighten-1" size="x-large" variant="flat" rounded="0">
                Get Exploration
            </v-btn>
        </div>
        <div class="d-block d-md-none">
            <v-menu>
                <template v-slot:activator="{ props }">
                    <v-btn icon="mdi-dots-vertical" v-bind="props"></v-btn>
                </template>
                    
                <v-list>
                    <v-list-item
                        v-for="(item, i) in items"
                        :key="i"
                    >
                        <v-list-item-title>{{ item.title }}</v-list-item-title>
                    </v-list-item>
                </v-list>
          </v-menu>
        </div>

    </v-app-bar>
</template>

<script setup>
    import {ref} from "vue"
    const items = ref([
            { title: 'Home page one' },
            { title: 'Home page two' },
            { title: 'Tour Grid' },
            { title: 'Tour List' },
            { title: 'Tour Single' },
            { title: 'Hotel' },
            { title: 'About' },
            { title: 'Team' },
            { title: 'Faq' },
            { title: '404' },
            { title: 'Blog' },
            { title: 'Contact' },
            { title: 'Get Exploration' }
    ]);
</script>

<style>
.expl {
    background-color: white ;
    color:#6347f9;
}
/* .v-toolbar__content {
  overflow-x: scroll !important;
} */
</style>