<template>
  <div>
    <v-container v-for="item in items" :key="item.val">
      <v-row class="background">
        <v-col :cols="item.val" class="white"> cols={{ item.val }} </v-col>
        <v-col :cols="item.val" class="red">
          red
        </v-col>
        <v-col :cols="item.val" class="blue">
          blue
        </v-col>
        <v-col :cols="item.val" class="yellow">
          yellow
        </v-col>
        <v-col :cols="item.val" xl="12" class="green">
          xl 12
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [{ val: 1 }, { val: 5 }, { val: "auto" }]
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
