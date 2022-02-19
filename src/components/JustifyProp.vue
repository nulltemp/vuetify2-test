<template>
  <div>
    <v-container v-for="item in items" :key="item.val" class="background">
      <v-row :justify="item.val">
        <v-col cols="2" class="white">
          {{ item.val }}
        </v-col>
        <v-col cols="2" class="red"> red </v-col>
        <v-col cols="2" class="blue font-fix"> blue </v-col>
      </v-row>
    </v-container>
    <v-container class="background">
      <v-row justify="center" justify-xl="space-between">
        <v-col cols="2" class="white"> justify-xl space-between </v-col>
        <v-col cols="2" class="red"> red </v-col>
        <v-col cols="2" class="blue font-fix"> blue </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { val: "start" },
        { val: "center" },
        { val: "end" },
        { val: "space-around" },
        { val: "space-between" }
      ]
    };
  }
};
</script>

<style scoped>
.font-fix {
  font-size: 3em;
}

.background {
  background-color: grey;
}
</style>
