<template>
<v-col justify="center" align="center">
    <v-row v-for="(item , name) in products" :key="name">
        <productsCard :title="name" :items="item.products" />
    </v-row>
</v-col>
</template>

<script>
import {
    products
} from '~/middleware/items'
import productsCard from '~/components/productsCard'
export default {
    components: {
        productsCard,
    },
    data: () => {
        return {
            products,
        }
    },
}
</script>
