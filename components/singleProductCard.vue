<template>
  <v-card class="col-10 col-md-4 ma-10 rounded-xl justify-center" color="#d6effa">
    <v-card-text>
      <v-row align="center" justify="center">
        <v-col>
          <v-img class="rounded-xl" :src="image" aspect-ratio="1" contain></v-img>
        </v-col>
        <v-col>
          <h1 style="color:black!important">{{title}}</h1>
        </v-col>
      </v-row>
    </v-card-text>

    <v-card-actions>
      <v-btn text color="deep-purple accent-4">Read more</v-btn>
      <v-spacer></v-spacer>
      <v-btn text disabled style="color:black!important">{{price}}TL</v-btn>
      <v-btn class="rounded-xl">Buy</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  props: {
    price: Number,
    title: String,
    description: String,
    image: String,
  },
}
</script>
