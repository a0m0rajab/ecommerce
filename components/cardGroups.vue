<template>
<v-col>
    <v-row justify="space-between">
        <h2>{{title}}</h2>
        <v-btn nuxt :to="title" text>More</v-btn>
    </v-row>
    <v-row>
        <v-slide-group show-arrows class="sm-3">
            <v-slide-item class="sm-3" v-for="(item, index) in items" :key="index" v-slot:default="{ toggle }">
                <v-card elevation="6" class="ma-3" :height="size" :width="size" @click="toggle" shaped>
                    <v-img class="white--text align-end" :height="size" :src="item.icon">
                        <v-card-title>{{item.icon}}</v-card-title>
                    </v-img>
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
        items: Array,
    },
    data: () => {
        return {
            size: 150,
        }
    },
    created: () => {
        console.log('created')
    },
}
</script>
