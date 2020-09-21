<template>
  <v-col>
    <v-row justify="space-between">
      <h2>{{title}}</h2>
      <v-btn nuxt :to="title" text>More</v-btn>
    </v-row>
    <v-row>
      <v-slide-group show-arrows class="sm-3" v-model="model">
        <v-slide-item
          class="sm-3"
          v-for="(item, name) in items"
          :key="name"
          v-slot:default="{ toggle }"
        >
          <v-card
            align="center"
            elevation="6"
            class="ma-3 d-flex flex-no-wrap justify-space-between"
            :height="size"
            :width="size"
            @click="toggle"
            shaped
          >
            <v-img shaped :src="imageName(item.image,item.name)"></v-img>
          </v-card>
        </v-slide-item>
      </v-slide-group>
      <v-expand-transition>
        <v-row justify="center">
          <singleProductCard
            class="sm-3"
            v-if="model != null"
            :title="name"
            :description="description"
            :image="link"
            :price="price"
          />
        </v-row>
      </v-expand-transition>
    </v-row>
  </v-col>
</template>

<script>
import singleProductCard from '~/components/singleProductCard'
import { products } from '~/middleware/items'

export default {
  components: {
    singleProductCard,
  },
  props: {
    title: String,
    items: Array,
  },
  data: () => {
    return {
      products,
      model: null,
      size: 200,
    }
  },
  created: () => {
    console.log('created')
  },
  methods: {
    imageName(link, name) {
      if (link.endsWith('jpg')) return link
      return `${link}/${name}/200`
    },
  },
  computed: {
    selectedObject() {
      return products[this.title].products[this.model]
    },
    name() {
      return this.selectedObject.name
    },
    description() {
      return this.selectedObject.description
    },
    link() {
      return this.imageName(this.selectedObject.image, this.selectedObject.name)
    },
    price() {
      return this.selectedObject.price
    },
  },
}
</script>
