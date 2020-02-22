<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn v-for="item in items" :key="item" text @click="selected = item">
        {{ item }}
      </v-btn>
    </v-app-bar>

    <v-content>
      <fluid v-if="selected === 'fluid'" />
      <align v-else-if="selected === 'align'" />
      <alignContent v-else-if="selected === 'alignContent'" />
      <dense v-else-if="selected === 'dense'" />
      <justify v-else-if="selected === 'justify'" />
      <no-gutters v-else-if="selected === 'noGutters'" />
      <align-self v-else-if="selected === 'alignSelf'" />
      <cols v-else-if="selected === 'cols'" />
      <offset v-else-if="selected === 'offset'" />
      <order v-else-if="selected === 'order'" />
      <hello-world v-else />
    </v-content>

    <v-footer dark>
      <v-spacer />
      <privacy-policy />
    </v-footer>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import Fluid from "./components/Fluid";
import Align from "./components/Align";
import AlignContent from "./components/AlignContent";
import Dense from "./components/Dense";
import Justify from "./components/Justify";
import NoGutters from "./components/NoGutters";
import AlignSelf from "./components/AlignSelf";
import Cols from "./components/Cols";
import Offset from "./components/Offset";
import Order from "./components/Order";
import PrivacyPolicy from "./components/modal/PrivacyPolicy";

export default {
  name: "App",
  components: {
    HelloWorld,
    Fluid,
    Align,
    AlignContent,
    Dense,
    Justify,
    NoGutters,
    AlignSelf,
    Cols,
    Offset,
    Order,
    PrivacyPolicy
  },
  data() {
    return {
      items: [
        "fluid",
        "align",
        "alignContent",
        "dense",
        "justify",
        "noGutters",
        "alignSelf",
        "cols",
        "offset",
        "order"
      ],
      selected: null
    };
  }
};
</script>
