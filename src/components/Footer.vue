<template>
  <footer class="footer container">
    <div class="footer__logo">
      <a  class="footer__logo-img">
        <img src="../assets/img/logo.png" alt="логотип компании">
        <img src="../assets/img/productly.svg" alt="productly">
      </a>
    </div>
    <div class="footer__menu">
      <nav class="footer__nav">
        <h3 class="footer__heading">Quick Links</h3>
        <ul class="footer__list">
          <li class="footer__item"><a href="#" class="footer__link">About Us</a></li>
          <li class="footer__item"><a href="#" class="footer__link">Blog</a></li>
          <li class="footer__item"><a href="#" class="footer__link">Contact</a></li>
          <li class="footer__item"><a href="#" class="footer__link">FAQ</a></li>
        </ul>
      </nav>
      <nav class="footer__nav">
        <h3 class="footer__heading">Legal Stuff</h3>
        <ul class="footer__list">
          <li class="footer__item"><a href="#" class="footer__link">Disclaimer</a></li>
          <li class="footer__item"><a href="#" class="footer__link">Financing</a></li>
          <li class="footer__item"><a href="#" class="footer__link">Privacy Policy</a></li>
          <li class="footer__item"><a href="#" class="footer__link"> Terms of Service</a></li>
        </ul>
      </nav>
    </div>
    <div class="footer__reply">
      <h3 class="footer__heading">Knowing you're always on the best energy deal.</h3>
      <form>
        <input
            type="text"
            v-model="userContact"
            placeholder="Enter your phone Number"
        >
        <button class="footer__btn btn btn--bright" type="submit">Sign up Now</button>
      </form>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'FooterComponent',
  data() {
    return {
      userContact: ''
    }
  }
}
</script>
<style lang="scss" scoped>
@import "../assets/sass/vars";

.footer {
  display: flex;
  padding-top: 102px;
  padding-bottom: 91px;
  position: relative;

  @media (max-width: 900px) {
    display: block;
    padding-top: 55px;
  }

  &:before {
    content: "";
    top: 0;
    left: 0;
    right: 0;
    margin: auto;
    height: 1px;
    width: 95%;
    background-color: rgba(188, 208, 229, 0.496913);
    position: absolute;
  }

  input {
    background: $color-default-white;
    border: 1px solid $color-light;
    box-sizing: border-box;
    border-radius: 4px;
    padding: 10px 15px;
    font-family: $secondary-font;
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 28px;
    width: 100%;
    max-width: 500px;
    margin-bottom: 30px;


    &::placeholder {
      color: $color-light;
    }
  }


  &__btn {
    font-weight: 700;
    display: block;
  }

  &__logo {
    margin-right: auto;

    @media (max-width: 900px) {
      margin-bottom: 30px;
    }

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
    flex-basis: 32.5%;
    margin-right: 82px;
    display: flex;
    justify-content: space-between;

    @media (max-width: 900px) {
      margin-right: 0;
      margin-bottom: 30px;
    }

    @media (max-width: 400px) {
      display: block;
    }
  }

  &__nav {
    width: calc(50% - 40px);

    @media (max-width: 400px) {
      width: auto;
      margin-bottom: 20px;
    }
  }

  &__reply {
    flex-basis: 27.5%;

    .footer__heading {
      max-width: 280px;
    }
  }

  &__list {
    margin: 0;
    padding: 0;
    list-style: none;
  }

  &__heading {
    font-family: $secondary-font;
    font-style: normal;
    font-weight: 700;
    font-size: 20px;
    line-height: 30px;
    color: $color-dark-base;
    margin: 0 0 35px 0;
  }

  &__link {
    font-family: $primary-font;
    font-style: normal;
    font-weight: 400;
    font-size: 16px;
    line-height: 35px;
    color: $color-dark-3;
    text-decoration: none;
  }
}
</style>
