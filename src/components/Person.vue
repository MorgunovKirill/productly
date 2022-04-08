<template>
  <div class="person">
      <p class="person__reply">{{ reply }}</p>
      <div class="person__img">
        <img :src="img" alt="author avatar">
      </div>
  </div>
</template>

<script>
export default {
  name: 'PersonComponent',
  props: ['reply', 'img']
}
</script>

<style lang="scss" scoped>
@import "../assets/sass/vars";

.person {
  position: absolute;

  @media (max-width: 1070px) {
    position: static;
    width: calc(33% - 20px);
    display: flex;
    flex-direction: column;
    margin-bottom: 30px;
  }

  @media (max-width: 960px) {
    width: calc(50% - 20px);
  }

  @media (max-width: 600px) {
    width: auto;
    max-width: 280px;
    margin-left: auto;
    margin-right: auto;
  }

  &:nth-child(1) {
    top: 116px;
    right: 15%;
  }

  &:nth-child(2) {
    top: 439px;
    right: 10%;
  }

  &:nth-child(3) {
    top: 561px;
    right: 35%;
  }

  &:nth-child(4) {
    top: 463px;
    right: 75%;
  }

  &:nth-child(5) {
    top: 181px;
    right: 70%;

    .person__img {
      right: initial;
      top: 60px;
      left: -50px;
    }

    .person__reply {

      &:before {
        right:  initial;
        left: 36px;

        @media (max-width: 1070px) {
          left: initial;
          right: 30px;
        }
      }
      &:after {
        right: initial;
        left: 30px;

        @media (max-width: 1070px) {
          left: initial;
          right: 30px;
        }
      }
    }
  }

  &__reply {
    position: relative;
    background: $color-default-white;
    box-shadow: 0 2px 8px rgba(86, 117, 146, 0.1);
    border-radius: 50px;
    padding: 14px 19px 15px 23px;
    width: fit-content;
    min-width: 240px;
    font-family: $primary-font;
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 24px;
    color: $color-dark-base;
    z-index: 1;
    margin: 0;

    @media (max-width: 960px) {
      align-self: flex-end;
    }


    &:before {
      content: "";
      position: absolute;
      width: 17px;
      height: 17px;
      border-radius: 50%;
      background-color: $color-default-white;
      bottom: -6px;
      right: 36px;
    }

    &:after {
      content: "";
      position: absolute;
      width: 9px;
      height: 9px;
      border-radius: 50%;
      background-color: $color-default-white;
      bottom: -17px;
      right: 30px;
    }
  }

  &__img {
    position: absolute;
    top: 55px;
    right: -45px;
    width: 98px;
    height: 98px;

    @media (max-width: 1070px) {
      position: static;
      align-self: flex-end;
    }
  }
}
</style>
