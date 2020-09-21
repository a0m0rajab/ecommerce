<template>
<v-app>
    <v-app-bar elevate-on-scroll class="rounded-b-xl" color="white" dense app>
        <v-menu offset-y content-class="rounded-xl">
            <template class="rounded-xl" v-slot:activator="{ on, attrs }">
                <v-app-bar-nav-icon v-bind="attrs" v-on="on" @click.stop="drawer = !drawer" />
            </template>
            <v-list>
                <v-list-item v-for="(item, index) in items" :key="index" nuxt :to="item.to" @click>
                    <v-icon>{{ item.icon }}</v-icon>
                    <v-list-item-title>{{item.title }}</v-list-item-title>
                </v-list-item>
            </v-list>
        </v-menu>
        <v-toolbar-title style="overflow:visible" v-text="title" />

        <v-responsive>
            <v-text-field label="Serah" v-model="search" dense flat hide-details prepend-inner-icon="mdi-magnify" rounded solo />
        </v-responsive>
    </v-app-bar>
    <v-main>
        <v-container>
            <nuxt />
        </v-container>
    </v-main>
    <v-footer absolute app>
        <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
</v-app>
</template>

<script>
import {
    products
} from '~/middleware/items'
console.log(products)
export default {
    data() {
        return {
            search: '',
            clipped: false,
            drawer: false,
            items: [{
                    icon: 'mdi-apps',
                    title: 'Welcome',
                    to: '/',
                },
                {
                    icon: 'mdi-chart-bubble',
                    title: 'Inspire',
                    to: '/inspire',
                },
            ],
            miniVariant: false,
            right: true,
            rightDrawer: false,
            title: 'Zenowa',
        }
    },
}
</script>
