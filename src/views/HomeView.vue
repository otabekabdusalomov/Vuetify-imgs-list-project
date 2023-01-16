<template>
  <v-app>
    <NavbarSection class="index" />
    <DashboardCard />
    <FooterSection />
  </v-app>
</template>

<script>
import NavbarSection from '../components/NavbarSection.vue'
import DashboardCard from '../components/DashboardCard.vue'
import FooterSection from '../components/FooterSection.vue'
import { defineComponent } from 'vue';


export default defineComponent({
  components: {
    NavbarSection,
    DashboardCard,
    FooterSection,
  },
});
</script>

<style>
.index {
  z-index: 9999;
}
</style>