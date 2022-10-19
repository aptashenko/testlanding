<template>
  <div class="comment">
    <div class="comment__top">
      <ul class="comment__leftSide">
        <li class="comment__title">
          {{title}}
        </li>
        <li class="comment__rating">
          <img v-for="(rate, i) of rating" :key="i" src="../assets/images/rating-star.svg" alt="star">
        </li>
      </ul>
      <ul class="comment__rightSide">
        <li class="comment__date">
          {{date}}
        </li>
        <li class="comment__name">
          {{name}}
        </li>
      </ul>
    </div>
    <div class="comment__body">
      <p class="comment__text">{{text}}</p>
    </div>
  </div>
</template>

<script>
export default {
  props: ['name', 'date', 'text', 'rating', 'title']
}
</script>

<style lang="scss">
.comment {
  padding: 15px;
  display: flex;
  flex-direction: column;
  background: #F9F9F9;
  border-radius: 9px;
  &:not(:last-child) {
    margin-bottom: 10px;
  }
  &__title {
    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 700;
    font-size: 14px;
    line-height: 150%;
    color: #111113;
    @media (max-width: 320px) {
        font-size: 12px;
      }
  }
  &__date, &__name {
    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 500;
    font-size: 12px;
    line-height: 150%;
    text-align: right;
    color: #111113;
    opacity: 0.5;
    @media (max-width: 320px) {
        font-size: 11px;
      }
  }
  &__top {
    display: flex;
    justify-content: space-between;
    align-items: baseline;
  }
  &__leftSide {
    padding: 0;
    margin: 0;
    list-style: none;
  }
  &__rightSide {
    padding: 0;
    margin: 0;
    margin-left: 20px;
    list-style: none;
  }
  &__body {
    margin-top: 15px;
  }
  &__text {
    margin: 0;
    font-family: 'SF Pro Text';
    font-style: normal;
    font-weight: 400;
    font-size: 12px;
    line-height: 150%;
    color: #111113;
    @media (max-width: 320px) {
        font-size: 9px;
      }
  }
}
</style>