<template>
  <div class="startPage">
    <div class="container">
          <h1 class="startPage__title">Enhance <span class="startPage__title--red">potency & stamina</span> with the #1 app for
            men's health!</h1>
          <VieoComp />
          <p class="startPage__stats">36k 5-star ratings | 1.8M+ downloads</p>
          <img class="startPage__rating" src="../assets/images/stats.jpg" alt="">
          <a href="#" class="startPage__button">Get the Dr. Kegel app</a>
    </div>
  </div>
</template>
<script>
import VieoComp from '@/components/VideoComp.vue';
export default {
  components: { VieoComp },
}
</script>
<style lang="scss">
.container {
  max-width: 615px;
  padding: 32px 32px 48px;
  margin: 0 auto;
  @media (max-width: 375px) {
    max-width: 375px;
    padding: 32px 32px 48px;
  }
}

.startPage {
  background: #000;

  &__title {
    margin: 0;
    text-align: center;
    font-family: 'SF Pro Display';
    font-style: normal;
    font-weight: 800;
    font-size: 30px;
    line-height: 135%;
    color: #FFFFFF;
    &--red {
      color: red;
      font-family: inherit;
    }
    @media (min-width: 450px) {
      padding: 0 46px;
    }
  }
  &__stats {
    font-family: 'SF Pro Text';
    margin: 0;
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 118.5%;
    text-align: center;
    color: #FFFFFF;
    opacity: 0.75;
    @media (max-width: 376px) {
      font-size: 14px;
    }
  }
  &__rating {
    display: block;
    width: 100%;
    width: 283px;
    max-width: 341px;
    margin: 10px auto 0;
  }
  &__button {
    display: block;
    margin: 48px auto 0;
    background: #FA2724;
    text-decoration: none;
    font-weight: 600;
    font-size: 22px;
    line-height: 1.2;
    text-align: center;
    color: #FFFFFF;
    border-radius: 109px;
    padding: 16px 34px;
    max-width: 311px;
    @media (max-width: 320px) {
      font-size: 16px;
    }
  }
}
</style>