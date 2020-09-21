<template>
<v-container fluid>
    <v-col justify="center" align="center">
        <v-row>
            <mainCard />
        </v-row>

        <v-row>
            <cardGroups title="Categories" :items="products" />
        </v-row>

        <v-row>
            <cardGroups title="Case studies" :items="products" />
        </v-row>
        <v-row>
            <information />
        </v-row>
    </v-col>
</v-container>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'
import mainCard from '~/components/mainCard'
import cardGroups from '~/components/cardGroups'
import information from '~/components/information'
import {
    products
} from '~/middleware/items'

export default {
    components: {
        Logo,
        VuetifyLogo,
        mainCard,
        cardGroups,
        information,
    },
    data: () => {
        return {
            products,
        }
    },
    created: () => {},
}
</script>
