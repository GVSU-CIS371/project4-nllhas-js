<template>
  <v-card>
    <v-banner color="success" top>
      <v-row class="text-center" justify="space-between">
        <v-col>
          <v-card-subtitle class="text-blue">
            {{ product.data.rating + "/5 customers recommend" }}
          </v-card-subtitle>
        </v-col>
        <v-col>
          <v-card-subtitle class="text-green">
            {{ "$" + product.data.price }}
          </v-card-subtitle>
        </v-col>
        <v-col>
          <v-card-subtitle class="text-brown">
            {{ product.data.stock + " In stock near you" }}
          </v-card-subtitle>
        </v-col>
      </v-row>
    </v-banner>
    <v-card-title class="text-center">
      {{ product.data.name }}
    </v-card-title>
    <v-img :src="product.data.image" aspect-ratio="1.7"></v-img>
    <v-card-text class="text-center">{{ product.data.description }}</v-card-text>
  </v-card>
</template>

<script lang="ts" setup>
import type { ProductDoc } from "../types/product";

type Props = {
  product: ProductDoc;
};

defineProps<Props>();
</script>
