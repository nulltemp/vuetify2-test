<template>
  <div>
    <v-container class="background">
      <v-row>
        <v-col>
          <v-card color="white">
            none
          </v-card>
        </v-col>
      </v-row>
    </v-container>

    <v-container fluid class="fluid-background">
      <v-row>
        <v-col>
          <v-card color="white">
            flued
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<style scoped>
.background {
  background-color: red;
}

.fluid-background {
  background-color: blue;
}
</style>
