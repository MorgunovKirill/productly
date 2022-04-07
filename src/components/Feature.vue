<template>
  <div class="feature">
    <div class="container">
      <div class="feature__info">
        <p class="feature__advantage">{{ options.advantage }}</p>
        <h2 class="feature__title">{{ options.title }}</h2>
        <p class="feature__description">{{ options.description }}</p>
        <ul class="feature__list" v-if="options.list">
          <li class="feature__item" v-for="(item, index) in options.list" :key="index">
            <h3 class="feature__heading">{{ item.heading }}</h3>
            <p class="feature__text">{{ item.text }}</p>
          </li>
        </ul>
      </div>
      <div class="feature__img">
        <img :src="options.img" alt="feature img">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'FeatureComponent',
  props: ['options'],
  mounted() {
    console.log(this.options)
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/sass/vars";

.feature {
  padding: 0;
  margin-bottom: 100px;

  .container {
    position: relative;
  }

  &__info {
    max-width: 486px;
  }

  &__advantage {
    font-family: $primary-font;
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 24px;
    color: $color-dark-3;
  }

  &__title {
    font-family: $primary-font;
    font-style: normal;
    font-weight: 700;
    font-size: 36px;
    line-height: 54px;
    max-width: 385px;
    margin: 0 0 25px 0;
    color: $color-dark-base;
  }

  &__description {
    font-family: $primary-font;
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 26px;
    color: $color-dark-3;
    margin: 0 0 30px 0;
  }

  &__list {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  &__heading {
    font-family: $primary-font;
    font-style: normal;
    font-weight: 700;
    font-size: 16px;
    line-height: 26px;
    color: $color-dark-base;
    margin: 0 0 12px 0;
  }

  &__item {
    font-family: $primary-font;
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 26px;
    color: $color-dark-3;
  }

  &__img {
    position: absolute;
    top: 0;
    right: 0;
  }
}
</style>
