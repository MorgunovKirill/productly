<template>
  <div id="app">
    <HeaderComponent />
  </div>
</template>

<script>
import HeaderComponent from "@/components/Header";

export default {
  name: 'App',
  components: {
    HeaderComponent,
  }
}
</script>
<style lang="scss">
@import 'assets/sass/base.scss';

</style>
