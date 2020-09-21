<template>
<v-card class="d-flex flex-column align-center justify-center">
    <v-icon large color="green darken-2">{{icon}}</v-icon>
    <v-card-title>{{title}}</v-card-title>
    <v-card-text>{{description}}</v-card-text>
</v-card>
</template>

<script>
export default {
    props: {
        title: String,
        description: String,
        icon: String,
    },
}
</script>
