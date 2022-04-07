<template>
  <div id="app">
    <HeaderComponent />
    <Intro />
  </div>
</template>

<script>
import HeaderComponent from "@/components/Header";
import Intro from "@/components/Intro";

export default {
  name: 'App',
  components: {
    Intro,
    HeaderComponent,
  }
}
</script>
<style lang="scss">
@import 'assets/sass/base.scss';

</style>
