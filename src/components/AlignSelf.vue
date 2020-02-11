<template>
  <div>
    <v-container>
      <v-row align="start" class="background">
        <v-col>
          align start
        </v-col>
        <v-col class="red">
          red
        </v-col>
        <v-col class="blue font-fix">
          blue
        </v-col>
        <v-col class="yellow" align-self="end">
          align-self end
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.font-fix {
  font-size: 3em;
}

.background {
  height: 10em;
  background-color: grey;
}
</style>
