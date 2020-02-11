<template>
  <div>
    <v-container v-for="item in items" :key="item.val">
      <v-row class="background">
        <v-col :offset="item.val" cols="1" class="white">
          offset={{ item.val }}
        </v-col>
        <v-col :offset="item.val" cols="1" class="red">
          red
        </v-col>
        <v-col :offset="item.val" cols="1" class="blue">
          blue
        </v-col>
        <v-col :offset="item.val" cols="1" class="yellow">
          yellow
        </v-col>
      </v-row>
    </v-container>
    <v-container>
      <v-row class="background">
        <v-col offset="1" offset-xl="5" cols="1" class="white">
          offset-xl=5
        </v-col>
        <v-col offset="1" offset-xl="5" cols="1" class="red">
          red
        </v-col>
        <v-col offset="1" offset-xl="5" cols="1" class="blue">
          blue
        </v-col>
        <v-col offset="1" offset-xl="5" cols="1" class="yellow">
          yellow
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [{ val: 1 }, { val: 3 }, { val: 5 }]
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
