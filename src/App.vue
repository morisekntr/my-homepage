<template>
  <v-app>
    <v-main>
      <HeaderComponent @navigate="scrollTo" />
      <CycleSlides />
      <BodyComponent />
      <FooterComponent @navigate="scrollTo" />
    </v-main>
  </v-app>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent.vue";
import CycleSlides from "./components/CycleSlides.vue";
import BodyComponent from "@/components/BodyComponent.vue";
import FooterComponent from "@/components/FooterComponent";

export default {
  name: 'App',

  components: {
    HeaderComponent,
    CycleSlides,
    BodyComponent,
    FooterComponent
  },
  methods: {
    scrollTo(section) {
      const element = document.getElementById(section);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
    }
  }
}
</script>
