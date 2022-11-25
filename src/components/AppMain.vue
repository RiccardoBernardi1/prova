<script>
import AppShops from "../components/AppShops.vue";
import AppContent from "../components/AppContent.vue";
import AppHero from "../components/AppHero.vue";

export default {
  name: "AppMain",
  components: {
    AppShops,
    AppContent,
    AppHero,
  },
};
</script>

<template>
  <main>
    <AppHero />
    <AppContent />
    <AppShops />
  </main>
</template>

<style scoped lang="scss">
main {
  background-color: #1c1c1c;
  color: white;
}
</style>
