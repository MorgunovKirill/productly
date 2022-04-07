<template>
  <section class="hero">
    <div class="container">
        <h2 class="hero__title">Need a super hero?</h2>
        <p class="hero__description">Do you require some help for your project: Conception workshop,
        prototyping, marketing strategy, landing page, Ux/UI?</p>
        <a class="btn btn--bright hero__btn">Contact our expert</a>
    </div>
  </section>
</template>

<script>
export default {
  name: 'HeroComponent',
}
</script>

<style lang="scss" scoped>
@import "../assets/sass/vars";

.hero {
    background-image: url("../assets/img/Bg-2.svg");
    background-repeat: no-repeat;
    background-position: 0 0;

    &__title {
        font-family: $primary-font;
        font-style: normal;
        font-weight: 700;
        font-size: 36px;
        line-height: 54px;
        margin: 0 0 20px 0;
    }
}
</style>
