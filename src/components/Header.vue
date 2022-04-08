<template>
  <header class="header container">
      <div class="header__logo">
        <a  class="header__logo-img">
          <img src="../assets/img/logo.png" alt="логотип компании">
          <img src="../assets/img/productly.svg" alt="productly">
        </a>
      </div>
      <button class="menu-toggler" type="button" @click="toggleMenu">
        <img src="../assets/img/burger.png" width="30" height="30" alt="">
      </button>
      <div
          class="header__menu"
          :class="{
            'header__menu--slide-in': isMenuOpen,
            'header__menu--slide-out': !isMenuOpen
          }"
      >
        <button class="menu-close" type="button" @click="closeMenu">
          <img src="../assets/img/clear.svg" width="16" height="16" alt="close menu">
        </button>
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
      </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponent',
  data() {
    return {
      isMenuOpen: false,
    }
  },
  methods: {
    toggleMenu() {
        this.isMenuOpen = !this.isMenuOpen

        if (this.isMenuOpen) {
          document.querySelector('body').classList.add('no-scroll');
        } else {
          document.querySelector('body').classList.remove('no-scroll');
        }
    },
    closeMenu() {
      this.isMenuOpen = false
      document.querySelector('body').classList.remove('no-scroll');
    }
  }
}
</script>
<style lang="scss" scoped>
  @import "../assets/sass/vars";

  .menu-toggler {
    display: none;
    border: none;
    background-color: $color-transparent;
    cursor: pointer;

    @media (max-width: 870px) {
      display: block;
    }
  }

  .menu-close {
    display: none;
    border: none;
    background-color: $color-transparent;
    cursor: pointer;
    position: absolute;
    top: 30px;
    right: 30px;

    @media (max-width: 870px) {
      display: block;
    }
  }

  .header {
    display: flex;
    align-items: center;
    padding-top: 24px;
    padding-right: 40px;
    padding-bottom: 26px;

    @media (max-width: 870px) {
      padding-right: 20px;
    }

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

    &__menu {
      display: flex;

      @media (max-width: 870px) {
        padding: 30px;
        display: block;
        position: fixed;
        top: 0;
        left: -317px;
        width: 317px;
        height: 100vh;
        background-color: $color-default-white;
        z-index: 1000;
        overflow: hidden;
      }

      &--slide-in {
        animation: slide-in 0.3s forwards;

        @media (max-width: 870px) {
          box-shadow: 0 0 5px $color-dark-base;
        }
      }

      &--slide-out {
        animation: slide-out 0.3s forwards;
      }

      @keyframes slide-in {
        100% {
          left: 0;
        }
      }

      @keyframes slide-out {
        0% {
          left: 0;
        }
        100% {
          left: -317px;
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

    @media (max-width: 870px) {
      margin-bottom: 50px;
    }

    &__list {
      margin: 0;
      padding: 0;
      list-style: none;
      display: flex;

      @media (max-width: 870px) {
        display: block;
      }
    }

    &__item {
      margin-right: 25px;

      @media (max-width: 870px) {
        margin-right: 0;
      }

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
