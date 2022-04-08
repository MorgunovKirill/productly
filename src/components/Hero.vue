<template>
  <section class="hero">
    <div class="container">
      <Person v-for="author in authors" :key="author.id" :reply="author.reply" :img="author.img" />
      <div class="hero__main">
        <h2 class="hero__title">Need a super hero?</h2>
        <p class="hero__description">Do you require some help for your project: Conception workshop,
          prototyping, marketing strategy, landing page, Ux/UI?</p>
        <a href="#" class="btn btn--bright hero__btn">Contact our expert</a>
      </div>
    </div>
  </section>
</template>

<script>
import Person from "@/components/Person";
import Avatar from "../assets/img/Avator.png";
import Avatar1 from "../assets/img/Avator-1.png";
import Avatar2 from "../assets/img/Avator-2.png";
import Avatar3 from "../assets/img/Avator-3.png";
import Avatar4 from "../assets/img/Avator-4.png";

export default {
  name: 'HeroComponent',
  components: {Person},
  data() {
    return {
      authors: [
        {
            id: 1,
            reply: 'I can help marketing strategy',
            img: Avatar,
        },
        {
            id: 2,
            reply: 'I can prototype your app',
            img: Avatar1,
        },
        {
             id: 3,
            reply: 'I will define the profile of your users',
            img: Avatar2,
        },
        {
            id: 4,
            reply: 'I can design you website',
            img: Avatar3,
        },
        {
             id: 5,
            reply: 'I can take care of your pitch',
            img: Avatar4,
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/sass/vars";

.hero {
    position: relative;
    background-image: url("../assets/img/Bg-2.svg");
    background-repeat: no-repeat;
    background-position: 0 0;
    background-size: 100%;
    padding: 230px 0 379px 0;

    &__title {
        font-family: $primary-font;
        font-style: normal;
        font-weight: 700;
        font-size: 36px;
        line-height: 54px;
        margin: 0 0 20px 0;
    }

    &__main {
      margin: 0 auto;
      max-width: 542px;
      text-align: center;
    }

    &__description {
      font-family: $primary-font;
      font-style: normal;
      font-weight: 500;
      font-size: 16px;
      line-height: 26px;
      color: $color-text-alt;
      margin: 0 0 34px 0;
    }

   &__btn {
     font-family: $primary-font;
     font-weight: 700;
   }
}
</style>
