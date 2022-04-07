<template>
  <div id="app">
    <HeaderComponent />
    <Intro />
    <Tools />
    <Feature :options="designFeature" />
    <Feature :options="marketersFeature" />
  </div>
</template>

<script>
import HeaderComponent from "@/components/Header";
import Intro from "@/components/Intro";
import Tools from "@/components/Tools";
import Feature from "@/components/Feature";
import designImage from "./assets/img/design-proffesionals.svg";
// import productManagersImage from "./assets/img/product-managers.svg";
import marketersImage from "./assets/img/marketers.svg";

export default {
  name: 'App',
  data() {
    return {
      designFeature: {
        advantage: 'Effortless Validation for',
        title: 'Design Professionals',
        description: 'The Myspace page defines the individual, his or her characteristics, traits, personal choices and the overall personality of the person.',
        img: designImage,
        list: [
          {heading: 'Accessory makers', text: 'While most people enjoy casino gambling, sports betting, lottery and bingo playing for the fun'},
          {heading: 'Alterationists', text: 'If you are looking for a new way to promote your business that won’t cost you more money,'},
          {heading: 'Custom Design designers', text: 'If you are looking for a new way to promote your business that won’t cost you more money, '},
        ]
      },
      marketersFeature: {
        advantage: 'Optimisation for',
        title: 'Marketers',
        img: marketersImage,
        description: 'Few would argue that, despite the advancements of feminism over the past three decades, women still face a double standard when it comes to their behavior.',
        list: [
          {heading: 'Accessory makers', text: 'While most people enjoy casino gambling, sports betting, lottery and bingo playing for the fun'},
          {heading: 'Alterationists', text: 'If you are looking for a new way to promote your business that won’t cost you more money,'},
          {heading: 'Custom Design designers', text: 'If you are looking for a new way to promote your business that won’t cost you more money'},
        ]
      },
    };
  },
  components: {
    Feature,
    Tools,
    Intro,
    HeaderComponent,
  }
}
</script>
<style lang="scss">
@import 'assets/sass/base.scss';

</style>
