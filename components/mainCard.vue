<template>
<v-card color="#d6effa" width="100%">
    <v-card-text>
        <v-row align="center">
            <v-col>
                <h1 style="color:black!important">The best commerce website</h1>
                <br />
                <h2>You will got the best from us</h2>
                <br />
                <v-responsive max-width="40vw">
                    <v-text-field label="Serah" v-model="search" dense flat hide-details prepend-inner-icon="mdi-magnify" rounded solo />
                </v-responsive>
            </v-col>
            <v-col md="4">
                <v-img src="undraw.svg" aspect-ratio="1.7" contain></v-img>
            </v-col>
        </v-row>
    </v-card-text>
</v-card>
</template>
