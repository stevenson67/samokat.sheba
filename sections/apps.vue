<template>
  <section class="apps">
    <div class="container">
      <h2 class="apps__title">И пока вы обдумываете<br> праздничное меню</h2>
      <span>Позаботьтесь о корме для кошки — закажите его в Самокате с доставкой<br> от 15 минут</span>
      <a href="https://vml8.adj.st/promocategory/0ee772cf-ba70-49ce-9f8d-1c1c80f0b0ed?showStories&showcaseType=MINIMARKET&adj_t=347ewp7"
         target="_blank" class="button">
        Перейти в приложение
      </a>
      <apps-details/>
    </div>
  </section>
</template>

<script>
export default {
  name: "apps"
}
</script>

<style lang="scss">
.apps {
  position: relative;
  margin-top: 24px;
  padding: 130px 0 80px 0;
  background-image: url('/media/details.svg');
  background-size: contain;
  background-repeat: no-repeat;
  background-position: top;
  &__details { display: none; }
  &__title {
    margin-bottom: 12px;
  }
  .button {
    margin-top: 40px;
  }
}
</style>
