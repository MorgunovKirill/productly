<template>
  <section class="tools">
    <div class="container">
      <h2 class="tools__title">We design tools to unveil your superpowers</h2>
      <ul class="tools__list">
        <li class="tools__item">
          <img src="../assets/img/icon-cursor.svg" alt="icon cursor">
          <h3 class="tools__heading">First click tests</h3>
          <p class="tools__text">While most people enjoy casino gambling,</p>
        </li>
        <li class="tools__item">
          <img src="../assets/img/icon-design.svg" alt="icon design">
          <h3 class="tools__heading">Design surveys</h3>
          <p class="tools__text">Sports betting, lottery and bingo playing for the fun</p>
        </li>
        <li class="tools__item">
          <img src="../assets/img/icon-heart.svg" alt="icon heart">
          <h3 class="tools__heading">Preference tests</h3>
          <p class="tools__text">The Myspace page defines the individual.</p>
        </li>
        <li class="tools__item">
          <img src="../assets/img/icon-time.svg" alt="icon hourglasses">
          <h3 class="tools__heading">Five second tests</h3>
          <p class="tools__text">Personal choices and the overall personality of the person. </p>
        </li>
      </ul>
      <a href="#" class="tools__btn btn btn--bright">Sign up now</a>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ToolsComponent',
}
</script>

<style lang="scss" scoped>
@import "../assets/sass/vars";

.tools {
  padding: 0 0 90px 0;
  margin-bottom: 140px;
  background-image: url("../assets/img/Bg.svg");
  background-position: 0 100%;
  background-size: contain;
  background-repeat: no-repeat;

  @media (max-width: 850px) {
    margin-bottom: 55px;
  }

  &__title {
    font-family: $primary-font;
    font-style: normal;
    font-weight: 700;
    font-size: 36px;
    line-height: 54px;
    max-width: 539px;
    margin: 0 auto 46px auto;
    color: $color-dark-base;
    text-align: center;
  }

  &__list {
    margin: 0 0 34px 0;
    padding: 0;
    list-style: none;
    display: flex;
    justify-content: space-between;

    @media (max-width: 850px) {
      flex-wrap: wrap;
      margin-bottom: 4px;
    }

    @media (max-width: 650px) {
      display: block;
    }
  }

  &__item {
    width: calc(25% - 46px);

    @media (max-width: 850px) {
      width: calc(50% - 46px);
      margin-bottom: 30px;
    }

    @media (max-width: 650px) {
      max-width: 280px;
      width: auto;
      margin-left: auto;
      margin-right: auto;
    }

    img {
      margin-bottom: 30px;
    }
  }

  &__heading {
    font-family: $primary-font;
    font-style: normal;
    font-weight: 600;
    font-size: 22px;
    line-height: 33px;
    margin: 0 0 13px 0;
  }

  &__text {
    font-family: $primary-font;
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 26px;
    color: $color-dark-3;
    margin: 0;
  }

  &__btn {
    display: block;
    width: fit-content;
    margin: 0 auto;
    font-weight: 700;
    font-family: $primary-font;
    text-transform: uppercase;
  }
}
</style>
