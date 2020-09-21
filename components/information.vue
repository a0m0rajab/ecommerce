<template>
<v-container fluid>
    <v-row>
        <h2>Our values</h2>
    </v-row>
    <v-row width="100%">
        <v-col v-for="(item,index) in items" :key="index" class="col-12 col-md-3">
            <v-item>
                <trustCard :title="item.title" :description="item.description" :icon="item.icon" />
            </v-item>
        </v-col>
    </v-row>
</v-container>
</template>

<script>
import trustCard from '~/components/trustCard'
export default {
    components: {
        trustCard,
    },
    data: () => {
        return {
            items: [{
                    title: 'Why us?',
                    description: 'We are the best in the coutnry, why not?',
                    icon: 'mdi-account-search-outline',
                },
                {
                    title: 'Fast delivery',
                    description: 'We deliver to everywhere just hire us',
                    icon: 'mdi-truck-delivery-outline',
                },
                {
                    title: 'Customer Focused',
                    description: 'We Focus about the value we add to our customer',
                    icon: 'mdi-account-arrow-left-outline',
                },
                {
                    title: 'Fast delivery',
                    description: 'We deliver to everywhere just hire us',
                    icon: 'mdi-truck-delivery-outline',
                },
            ],
        }
    },
}
</script>
