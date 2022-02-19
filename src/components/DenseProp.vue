<template>
  <div>
    <v-container v-for="item in items" :key="item.val">
      <v-row :dense="item.val" class="background">
        <v-col cols="2" class="white"> dense={{ item.val }} </v-col>
        <v-col cols="2" class="red">
          dDGZnj65xDmeteexauRphT8pph3fMRteXzcYEj4nQwTTYffZ5u
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [{ val: false }, { val: true }]
    };
  }
};
</script>

<style scoped>
.background {
  word-wrap: break-word;
}
</style>
