<template>
  <div>
    <v-container v-for="item in items" :key="item.val">
      <v-row :align="item.val" class="row-height">
        <v-col>
          {{ item.val }}
        </v-col>
        <v-col class="red"> red </v-col>
        <v-col class="blue font-fix"> blue </v-col>
      </v-row>
    </v-container>
    <v-container>
      <v-row align="center" align-xl="stretch" class="row-height">
        <v-col> align-xl stretch </v-col>
        <v-col class="red"> red </v-col>
        <v-col class="blue font-fix"> blue </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { val: "baseline" },
        { val: "start" },
        { val: "center" },
        { val: "end" },
        { val: "stretch" }
      ]
    };
  }
};
</script>

<style scoped>
.row-height {
  height: 100px;
}

.font-fix {
  font-size: 3em;
}
</style>
