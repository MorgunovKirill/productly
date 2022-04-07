<template>
  <header class="header container">
      <div class="header__logo">
        <a  class="header__logo-img">
          <img src="../assets/img/logo.png" alt="логотип компании">
          <img src="../assets/img/productly.svg" alt="productly">
        </a>
      </div>
      <nav class="main-nav">
        <ul class="main-nav__list">
          <li class="main-nav__item">
            <a href="#" class="main-nav__link">Product</a>
          </li>
          <li class="main-nav__item">
            <a href="#" class="main-nav__link">Customers</a>
          </li>
          <li class="main-nav__item">
            <a href="#" class="main-nav__link">Pricing</a>
          </li>
          <li class="main-nav__item">
            <a href="#" class="main-nav__link">Resources</a>
          </li>
        </ul>
      </nav>
      <nav class="user-nav">
        <a href="#" class="btn user-nav__btn">Sign In</a>
        <a href="#" class="btn btn--bright user-nav__btn user-nav__btn--logout">Sign Up</a>
      </nav>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponent',
}
</script>
<style lang="scss" scoped>
  @import "../assets/sass/vars";

  .header {
    display: flex;
    align-items: center;
    padding: 24px 40px 26px 0;

    &__logo {
      margin-right: auto;

      &-img {
        display: flex;
        align-items: center;

         img {
           &:last-child {
             margin-left: 10px;
             margin-top: 5px;
           }
         }
      }
    }
  }

  .main-nav {
    font-family: $primary-font;
    font-style: normal;
    font-weight: 400;
    font-size: 14px;
    line-height: 28px;
    margin-right: 29px;

    &__list {
      margin: 0;
      padding: 0;
      list-style: none;
      display: flex;
    }

    &__item {
      margin-right: 25px;

      &:last-child {
        margin-right: 0;
      }
    }

    &__link {
      text-decoration: none;
      color: $color-dark-base;
    }
  }

  .user-nav {
    font-family: $primary-font;
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 24px;

    &__btn {
      margin-right: 14px;

      &--logout {
        margin-right: 0;
      }
    }
  }
</style>
