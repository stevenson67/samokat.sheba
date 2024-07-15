<template>
  <aside class="result">
    <div class="result__header container">
      <logo color="var(--gray-4)"/>
      <div class="result__close" @click="$emit('close')">
        <close/>
      </div>
    </div>
    <div class="result__wrap result-gift">
<!--      <gift/>-->
      <gift-success/>
      <div class="container">
        <h2 class="result-gift__title">Поздравляем, вы стали <span>участником!</span></h2>
      </div>
    </div>
  </aside>
</template>

<script>
import MiniElka from "@/components/mini-elka";
import Logo from "@/components/logo";
import Close from "@/components/close";
import Gift from "@/components/gift";
import HandsElka from "@/components/hands-elka";
import GiftSuccess from "@/components/gift-success";
export default {
  name: "result",
  components: {GiftSuccess, HandsElka, Gift, Close, Logo, MiniElka},
  props: {
    code: String,
  },
}
</script>

<style lang="scss">
.result {
  position: fixed;
  top: 0; left: 0;
  width: 100%; height: 100%;
  z-index: 999;
  background: var(--green);
  display: flex;
  flex-direction: column;
  text-align: center;

  &.sorry { background: var(--lime); }

  &__header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    height: 28px;
    margin-top: 24px;
  }
  &__close {
    display: flex;
    cursor: pointer;
  }
  &__wrap {
    flex: 1;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    position: relative;

    span {
      padding: 2px 8px;
      border-radius: 6px;
    }
    .button {
      border-radius: 0;
      position: absolute;
      left: 0; bottom: 0;
      width: 100%;
      max-width: unset;
    }
  }
  &-wait {
    &__title {
      margin-top: 40px;
    }
  }
  &-gift {
    &__title {
      span {
        color: var(--yellow);
      }
    }
    p { color: var(--gray-4); }
  }
}
</style>
