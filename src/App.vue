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

    <v-main>
      <fluid-prop v-if="selected === 'fluid'" />
      <align-prop v-else-if="selected === 'align'" />
      <alignContent-prop v-else-if="selected === 'alignContent'" />
      <dense-prop v-else-if="selected === 'dense'" />
      <justify-prop v-else-if="selected === 'justify'" />
      <no-gutters-prop v-else-if="selected === 'noGutters'" />
      <align-self-prop v-else-if="selected === 'alignSelf'" />
      <cols-prop v-else-if="selected === 'cols'" />
      <offset-prop v-else-if="selected === 'offset'" />
      <order-prop v-else-if="selected === 'order'" />
      <hello-world v-else />
    </v-main>

    <v-footer dark>
      <v-spacer />
      <privacy-policy />
    </v-footer>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import FluidProp from "./components/FluidProp";
import AlignProp from "./components/AlignProp";
import AlignContentProp from "./components/AlignContentProp";
import DenseProp from "./components/DenseProp";
import JustifyProp from "./components/JustifyProp";
import NoGuttersProp from "./components/NoGuttersProp";
import AlignSelfProp from "./components/AlignSelfProp";
import ColsProp from "./components/ColsProp";
import OffsetProp from "./components/OffsetProp";
import OrderProp from "./components/OrderProp";
import PrivacyPolicy from "./components/modal/PrivacyPolicy";

export default {
  name: "App",
  components: {
    HelloWorld,
    FluidProp,
    AlignProp,
    AlignContentProp,
    DenseProp,
    JustifyProp,
    NoGuttersProp,
    AlignSelfProp,
    ColsProp,
    OffsetProp,
    OrderProp,
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
