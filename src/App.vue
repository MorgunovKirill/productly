<template>
  <div id="app">
    <HeaderComponent />
    <Intro />
    <Tools />
    <FeaturesList />
    <Hero />
    <Strategies />
    <Footer />
  </div>
</template>

<script>
import HeaderComponent from "@/components/Header.vue";
import Intro from "@/components/Intro.vue";
import Tools from "@/components/Tools.vue";
import FeaturesList from '@/components/FeaturesList.vue';
import Hero from '@/components/Hero.vue';
import Strategies from "@/components/Strategies";
import Footer from "@/components/Footer";

export default {
  name: 'App',
  components: {
    Footer,
    Strategies,
    Tools,
    Intro,
    HeaderComponent,
    FeaturesList,
    Hero
  }
}
</script>
<style lang="scss">
@import 'assets/sass/base.scss';

</style>
