<template>
  <div>
    <v-container v-for="item in items" :key="item.val">
      <v-row :align-content="item.val" class="background">
        <v-col cols="2" class="white">
          {{ item.val }}
        </v-col>
        <v-col cols="5" class="red"> red </v-col>
        <v-col cols="5" class="blue"> blue </v-col>
        <v-col cols="5" class="yellow"> yellow </v-col>
      </v-row>
    </v-container>
    <v-container>
      <v-row
        align-content="center"
        align-content-xl="stretch"
        class="background"
      >
        <v-col cols="2" class="white"> align-content-xl stretch </v-col>
        <v-col cols="5" class="red"> red </v-col>
        <v-col cols="5" class="blue"> blue </v-col>
        <v-col cols="5" class="yellow"> yellow </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { val: "center" },
        { val: "start" },
        { val: "end" },
        { val: "space-around" },
        { val: "space-between" },
        { val: "stretch" }
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
