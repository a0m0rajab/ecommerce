<template>
<v-col>
    <v-row justify="space-between">
        <h2>Hello world</h2>
        <h3>Show All</h3>
    </v-row>
    <v-row>
        <v-slide-group multiple show-arrows>
            <v-slide-item v-for="n in 15" :key="n" v-slot:default="{ active, toggle }">
                <v-card elevation="6" class="ma-4" height="200" width="200" @click="toggle" shaped>
                    <v-img class="white--text align-end" height="200px" src="https://cdn.vuetifyjs.com/images/cards/docks.jpg">
                        <v-card-title>beaches</v-card-title>
                    </v-img>
                    <v-scale-transition>
                        <v-icon v-if="active" color="white" size="48" v-text="'mdi-close-circle-outline'"></v-icon>
                    </v-scale-transition>
                </v-card>
            </v-slide-item>
        </v-slide-group>
    </v-row>
</v-col>
</template>
