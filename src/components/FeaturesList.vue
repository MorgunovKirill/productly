<template>
    <section class="features">
    <template v-for="option in features">
        <Feature :key="option.id" :options="option" />
    </template>
    </section>
</template>

<script>
import Feature from "@/components/Feature";
import designImage from "../assets/img/design-proffesionals.svg";
import productManagersImage from "../assets/img/product-managers.svg";
import marketersImage from "../assets/img/marketers.svg";


export default {
  name: 'FeatureList',
  data() {
    return {
        features: [
        {
            id: 1,
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
        {
                id: 2,
            alt: true,
            advantage: 'Easier decision making for',
            title: 'Product Managers',
            description: 'The Myspace page defines the individual, his or her characteristics, traits, personal choices and the overall personality of the person. ',
            img: productManagersImage,
            list: [
            {heading: 'Accessory makers', text: 'Never worry about overpaying for your energy again.'},
            {heading: 'Alterationists', text: 'We will only switch you to energy companies that we trust and will treat you right'},
            {heading: 'Custom Design designers', text: 'We track the markets daily and know where the savings are.'},
            ]
        },
        {
             id: 3,
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
        ]
    };
  },
  components: {
    Feature,
  }
}
</script>
