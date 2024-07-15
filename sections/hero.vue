<template>
  <section class="hero">
    <div class="container">
      <a class="hero__logo" href="/">
        <logo/>
      </a>
      <h1 class="hero__title">Что ждёт <span>вашего питомца</span> под ёлкой</h1>
      <div class="hero__subtitle">
        Заказывайте Sheba® в Самокате и участвуйте в розыгрыше призов
      </div>
      <div class="button start">Ввести код и получить подарок</div>
    </div>
  </section>
</template>

<script>
import Logo from "@/components/logo";
export default {
  name: "hero",
  components: {Logo}
}
</script>

<style lang="scss">
.hero {
  position: relative;
  &__logo {
    display: flex;
    justify-content: center;
    margin: 28px 0 56px 0;
  }
  &__title {
    margin: 16px 0;
    text-align: start;
    span {
      color: var(--yellow);
    }
  }
  .button { display: none; }
}
</style>
