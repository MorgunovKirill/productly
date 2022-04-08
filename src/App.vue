<template>
  <div id="app">
    <HeaderComponent />
    <Intro />
    <Tools />
    <FeaturesList />
    <Hero />
    <Strategies />
  </div>
</template>

<script>
import HeaderComponent from "@/components/Header.vue";
import Intro from "@/components/Intro.vue";
import Tools from "@/components/Tools.vue";
import FeaturesList from '@/components/FeaturesList.vue';
import Hero from '@/components/Hero.vue';
import Strategies from "@/components/Strategies";

export default {
  name: 'App',
  components: {
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
