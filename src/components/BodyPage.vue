<template>
  <div class="bodyPage">
    <div class="container">
        <h2 class="bodyPage__title">Simply train your intimate muscles to the rhythm of phone vibrations</h2>
        <img class="bodyPage__image" src="../assets/images/body-bg.jpg" alt="">
        <p class="bodyPage__text">“These muscles are responsible for male potency & stamina”</p>
        <ul class="bodyPage__list">
            <li class="bodyPage__item">
                <p class="bodyPage__benefit">Workouts take just <span class="bodyPage__benefit--bold">5 minutes a day</span></p>
            </li>
            <li class="bodyPage__item">
                <p class="bodyPage__benefit">You can <span class="bodyPage__benefit--bold">exercise in any place & situation:</span> lying on the couch, sitting at work, or standing in the bust</p>
            </li>
        </ul>
        <template v-for="comment of comments" >
            <CommentsComp
            :key="comment.name"
             :name="comment.name"
             :date="comment.date"
             :text="comment.text"
             :title="comment.title"
             :rating="comment.rating"
            />
        </template>
    </div>
  </div>
</template>

<script>
import CommentsComp from './CommentsComp.vue';
import comments from '../mixins/comments';
export default {
    components: { CommentsComp },
    mixins: [comments],
}
</script>

<style lang="scss">
.bodyPage {
    &__title {
        font-family: 'SF Pro Display';
        font-style: normal;
        font-weight: 600;
        font-size: 25px;
        line-height: 135%;
        text-align: center;    
        color: #111113;
        margin: 0;
    }
    &__image {
        display: block;
        width: 100%;
        margin: 15px auto 10px;
    }
    &__text {
        text-align: center;
        font-family: 'SF Pro Text';
        font-style: italic;
        font-weight: 400;
        font-size: 14px;
        line-height: 150%;
        text-align: center;
        color: #111113;
        margin: 0 auto 25px;
    }
    &__list {
        margin: 0 auto 32px;
        padding: 0;
        list-style: none;
    }
    &__item {
        display: flex;
        align-items: center;
        &::before {
            display: block;
            content: '';
            background: url('../assets/images/list.svg');
            background-repeat: no-repeat;
            background-size: contain;
            height: 24px;
            min-width: 24px;
            margin-right: 20px;
        }
        &:not(:last-child) {
            margin-bottom: 15px;
        }
    }
    &__benefit {
        margin: 0;
        font-family: 'SF Pro Text';
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 150%;
        color: #111113;
        &--bold {
            font-weight: 600;
        }
    }
}
</style>