<template>
  <div class="startPage">
    <div class="container">
          <h1 class="startPage__title">Enhance <span class="startPage__title--red">potency & stamina</span> with the #1 app for
            men's health!</h1>
          <video ref="player" class="startPage__video" src="../assets/video/timer.mp4" autoplay loop>
            Sorry, your browser doesn't support this video
          </video>
          <p class="startPage__stats">36k 5-star ratings | 1.8M+ downloads</p>
          <img class="startPage__rating" src="../assets/images/stats.jpg" alt="">
          <a href="#" class="startPage__button">Get the Dr. Kegel app</a>
    </div>
  </div>
</template>

<script>

export default {
}
</script>

<style lang="scss">
.container {
  max-width: 375px;
  padding: 32px 32px 48px;
  margin: 0 auto;
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
  }
  &__video {
    max-width: 100%;
    margin: 32px auto;
    display: block;
    border: 2px solid #fff;
  }
  &__stats {
    text-align: center;
    color: #fff;
    opacity: 0.75;
    margin: 0 auto;
  }
  &__rating {
    width: 100%;
    margin-top: 10px;
  }
  &__button {
    display: block;
    margin-top: 48px;
    background: #FA2724;
    text-decoration: none;
    font-weight: 600;
    font-size: 22px;
    line-height: 1.2;
    text-align: center;
    color: #FFFFFF;
    border-radius: 109px;
    padding: 16px 42px;
    @media (max-width: 320px) {
      font-size: 16px;
    }
  }
}
</style>