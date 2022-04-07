<template>
  <div id="app">
    <HeaderComponent />
    <Intro />
    <Tools />
    <FeaturesList />
  </div>
</template>

<script>
import HeaderComponent from "@/components/Header";
import Intro from "@/components/Intro";
import Tools from "@/components/Tools";
import FeaturesList from './components/FeaturesList.vue';

export default {
  name: 'App',
  components: {
    Tools,
    Intro,
    HeaderComponent,
    FeaturesList,
  }
}
</script>
<style lang="scss">
@import 'assets/sass/base.scss';

</style>
