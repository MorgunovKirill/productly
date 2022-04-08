<template>
  <section class="strategies">
    <div class="container">
        <h2 class="strategies__title">Marketing Strategies</h2>
        <p class="strategies__description">Join 40,000+ other marketers and get proven strategies on email marketing</p>
      <ul class="strategies__list">
        <li class="strategies__item" v-for="item in tabs" :key="item.id">
          <a href="#"
             class="strategies__link"
             @focus="changeTab(item.id)"
             @click.prevent="changeTab(item.id)"
             @blur="changeTab(null)"
          >
            <img :src="item.img" :alt="item.alt">
            <p class="strategies__info">By <b>Abdullah</b>  |  03 March 2019</p>
            <h3 class="strategies__heading">{{ item.title }}</h3>
        </a></li>
      </ul>
      <div class="strategies__tabs">
        <span
            class="strategies__dot"
            :class="{'strategies__dot--active': item.id === activeTab }"
            type="button"
            v-for="item in tabs"
            :key="item.id"></span>
      </div>
    </div>
  </section>
</template>

<script>
import StrategyImg1 from "../assets/img/strategy1.png";
import StrategyImg2 from "../assets/img/strategy2.png";
import StrategyImg3 from "../assets/img/strategy3.png";

export default {
  name: 'StrategiesComponent',
  data() {
    return {
      tabs: [
        {
          id: 1,
          title: 'Increasing Prosperity With Positive Thinking',
          img: StrategyImg1,
          alt: 'prosperity'
        },
        {
          id: 2,
          title: 'Motivation Is The First Step To Success',
          img: StrategyImg2,
          alt: 'motivation'
        },
        {
          id: 3,
          title: 'Success Steps For Your Personal Or Business Life',
          img: StrategyImg3,
          alt: 'success'
        },
      ],
      activeTab: null,
    }
  },
  methods: {
    changeTab(id) {
        this.activeTab = id
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/sass/vars";

.strategies {
  padding-bottom: 137px;

  &__title {
    font-family: $primary-font;
    font-style: normal;
    font-weight: 700;
    font-size: 34px;
    line-height: 51px;
    color: $color-dark-base;
    margin: 0 0 9px 0;
  }

  &__description {
    font-family:  $primary-font;
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 26px;
    color: $color-dark-3;
    margin: 0 0 55px 0;
  }

  &__list {
    margin: 0 0 45px 0;
    padding: 0;
    list-style: none;
    display: flex;
    justify-content: space-between;
  }

  &__item {
    width: calc(33% - 32px);
    max-width: 348px;
  }

  &__link {
    font-family: $primary-font;
    font-style: normal;
    color: $color-dark-base;
    text-decoration: none;
    outline: none;

    img {
      margin-bottom: 30px;
    }

    &:hover,
    &:focus {

      .strategies__heading {
        color: $color-bright;
      }
    }
  }

  &__info {
    margin: 0 0 12px 0;
  }

  &__heading {
    font-weight: 700;
    font-size: 24px;
    line-height: 34px;
    margin: 0;
    transition: color 0.3s ease;
  }

  &__tabs {
    display: flex;
    width: fit-content;
    margin: 0 auto;
  }

  &__dot {
    border: none;
    width: 16px;
    height: 16px;
    border-radius: 50%;
    background-color: #efefef;
    transition: color 0.3s ease;
    margin-right: 10px;

    &:last-child {
      margin-right: 0;
    }

    &--active {
      background-color: $color-bright;
    }
  }
}
</style>
