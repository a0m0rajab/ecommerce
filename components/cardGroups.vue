<template>
<v-col>
    <v-row justify="space-between">
        <h2>{{title}}</h2>
        <v-btn nuxt :to="title" text>More</v-btn>
    </v-row>
    <v-row>
        <v-slide-group show-arrows class="sm-3">
            <v-slide-item class="sm-3" v-for="(item, name) in items" :key="name" v-slot:default="{ toggle }">
                <v-card align="center" elevation="6" class="ma-3 d-flex align-center" :height="size" :width="size" @click="toggle" shaped>
                    <v-col class="d-flext justify-center">
                        <v-row class="d-flext justify-center">
                            <v-icon large color="green darken-2">{{item.icon}}</v-icon>
                        </v-row>
                        <v-row class="d-flext justify-center">
                            <v-card-title>{{name}}</v-card-title>
                        </v-row>
                    </v-col>
                </v-card>
            </v-slide-item>
        </v-slide-group>
    </v-row>
</v-col>
</template>

<script>
export default {
    props: {
        title: String,
        items: Object,
    },
    data: () => {
        return {
            size: 160,
        }
    },
    created: () => {
        console.log('created')
    },
}
</script>
