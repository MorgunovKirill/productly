<template>
  <section class="intro container">
    <h2 class="intro__title">The Design Thinking superpowers</h2>
    <p class="intro__description">Tools, tutorials, design and innovation experts, all in one place! The most intuitive
      way to imagine your next user experience.</p>
    <div class="intro__options">
      <a href="#" class="btn btn--bright">Get started</a>
      <a href="#" class="intro__video-link">
        <img src="../assets/img/icon-play.svg" alt="icon play">
        <span>Watch the Video</span>
      </a>
    </div>
  </section>
</template>

<script>
export default {
  name: 'IntroComponent',
}
</script>

<style lang="scss" scoped>
@import "../assets/sass/vars";

.intro {
  padding-top: 116px;
  padding-bottom:  108px;
  padding-left: 55px;
  margin-top: 33px;
  margin-bottom: 115px;
  background-image: url("../assets/img/intro.svg");
  background-repeat: no-repeat;
  background-position: 100% 0;

  @media (max-width: 1100px) {
    padding-bottom: 500px;
    background-position: 50% 100%;
    margin-bottom: 75px;
  }

  @media (max-width: 650px) {
    background: none;
    padding-top: 0;
    padding-bottom: 0;
    padding-left: 20px;
  }

  &__title {
    font-family: $primary-font;
    font-style: normal;
    font-weight: 700;
    font-size: 44px;
    line-height: 54px;
    max-width: 518px;
    margin: 0 0 30px 0;
    color: $color-dark-base;

    @media (max-width: 650px) {
     font-size: 36px;
    }
  }

  &__description {
    font-family: $primary-font;
    font-style: normal;
    font-weight: 400;
    font-size: 18px;
    line-height: 28px;
    color: $color-dark-3;
    max-width: 458px;
    margin: 0 0 45px 0;
  }

  &__options {
    display: flex;
    align-items: center;

    @media (max-width: 650px) {
      flex-direction: column;
    }

    .btn {
      font-weight: 700;
      font-family: $primary-font;
      margin-right: 30px;

      @media (max-width: 650px) {
        font-size: 14px;
        margin-right: 0;
        margin-bottom: 20px;
      }
    }
  }

  &__video-link {
    display: flex;
    font-family: $primary-font;
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 24px;
    text-decoration-line: underline;
    color: $color-bright;

    img {
      margin-right: 8.5px;
    }
  }
}
</style>
