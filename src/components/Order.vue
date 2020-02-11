<template>
  <div>
    <v-container v-for="(item, index) in items" :key="index">
      <v-row class="background">
        <v-col order="0" cols="1" class="white"> order={{ item }} </v-col>
        <v-col :order="item[0]" cols="1" class="red">
          red order={{ item[0] }}
        </v-col>
        <v-col :order="item[1]" cols="1" class="blue">
          blue order={{ item[1] }}
        </v-col>
        <v-col :order="item[2]" cols="1" class="yellow">
          yellow order={{ item[2] }}
        </v-col>
        <v-col :order="item[3]" order-xl="last" cols="1" class="green">
          order-xl=last order={{ item[3] }}
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        [1, 2, 3, 4],
        [4, 3, 2, 1]
      ]
    };
  }
};
</script>

<style scoped>
.background {
  height: 10em;
  background-color: grey;
}
</style>
