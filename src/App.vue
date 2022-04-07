<template>
  <div id="app">
    <HeaderComponent />
    <Intro />
    <Tools />
  </div>
</template>

<script>
import HeaderComponent from "@/components/Header";
import Intro from "@/components/Intro";
import Tools from "@/components/Tools";

export default {
  name: 'App',
  components: {
    Tools,
    Intro,
    HeaderComponent,
  }
}
</script>
<style lang="scss">
@import 'assets/sass/base.scss';

</style>
