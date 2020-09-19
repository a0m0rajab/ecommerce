<template>
<v-container fluid>
    <v-row justify="center" align="center">
        <v-col cols="12">
            <mainCard />
        </v-col>

        <v-col cols="12">
            <cardGroups />
        </v-col>

        <v-col cols="12">
            <cardGroups />
        </v-col>
        <v-col>
            <information />
        </v-col>
    </v-row>
</v-container>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'
import mainCard from '~/components/mainCard'
import cardGroups from '~/components/cardGroups'
import information from '~/components/information'

export default {
    components: {
        Logo,
        VuetifyLogo,
        mainCard,
        cardGroups,
        information,
    },
}
</script>
