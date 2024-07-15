<template>
  <section class="elka">
    <div class="elka__top">
      <elka-top/>
      <div class="button start">Ввести код и получить подарок</div>
    </div>
    <div class="elka__middle">
      <div class="elka__middle__wrap">
        <h2 class="elka__middle__title">Порадовать <span>любимца</span> просто</h2>
        <div class="elka__middle__list">
          <ul>
            <strong>Правила розыгрыша:</strong>
            <li>
              <i>1</i>
              <span>Выберите корм от Sheba® на сумму от 200 ₽</span>
            </li>
            <li>
              <i>2</i>
              <span>Получите СМС с кодом для участия в акции. Если оно не пришло, разрешите нам отправку СМС в настройках</span>
            </li>
            <li>
              <i>3</i>
              <span>Введите код в поле под ёлкой</span>
            </li>
            <li>
              <i>4</i>
              <span>Ждите результатов 25 декабря</span>
            </li>
            <a href="https://terms.samokat.ru/promo/Pravila_Samokat_Rozygrysh_prizov_dlya_koshki.pdf" target="_blank">Подробнее о правилах</a>
          </ul>
        </div>
      </div>
    </div>
    <div class="elka__bottom">
      <elka-bottom/>
      <div class="elka__list">
        <div class="elka__item">
          <div class="elka__image">
            <img src="../static/media/elka-bottom/elka-list.png">
          </div>
          <div class="elka__text">
            <h2>За <span>один</span> заказ</h2>
            <p>Выиграйте промокод на скидку в Самокате</p>
          </div>
        </div>
        <div class="elka__item">
          <div class="elka__image">
            <img src="../static/media/elka-bottom/elka-list1.png">
          </div>
          <div class="elka__text">
            <h2>За <span>два</span> заказа</h2>
            <p>Ловите шанс получить сертификат в зоомагазин</p>
          </div>
        </div>
        <div class="elka__item">
          <div class="elka__image">
            <img src="../static/media/elka-bottom/elka-list2.png">
          </div>
          <div class="elka__text">
            <h2>За <span>три</span> заказа</h2>
            <p>Участвуйте в розыгрыше уютной лежанки</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import ElkaTop from "~/components/elka-top";
import ElkaBottom from "@/components/elka-bottom";
export default {
  name: "elka",
  components: {ElkaBottom, ElkaTop}
}
</script>

<style lang="scss">
.elka {
  position: relative;
  &__image {
    width: 100%;
    object-fit: contain;
    z-index: -1;
  }
  &__top {
    position: relative;
    margin-top: -5%;
    width: 100%;
    overflow: hidden;
    .elka-svg {
      width: 190%;
      margin-left: -47%;
      margin-bottom: -119%;
    }
    .star {
      display: none;
    }
    .button {
      position: absolute;
      left: 50%; top: 45%;
      transform: translate(-50%, -50%);
      width: 85%;
      max-width: 325px;
    }
  }
  &__bottom {
    position: relative;
    overflow: hidden;
    margin-top: -15%;
    margin-left: -8%;
    margin-bottom: 0;
    .elka-svg {
      width: 150%;
      margin-left: -22%;
    }
    .elka__list {
      position: absolute;
      left: 50%;
      top: 45%;
      transform: translate(-50%, -50%);
      width: 85%;
      max-width: 325px;
      z-index: 3;
    }
    .elka__item {
      display: flex;
    }
    .elka__image {
      width: 30%;
      img {
        width: 77px;
        height: 77px;
      }
    }
    .elka__text {
      width: 70%;
      span {
        color: var(--yellow);
      }
    }
  }
  &-svg {
    display: block;
    width: 130%;
    margin-left: -15%;
    height: auto;
    position: relative;
    z-index: -1;
    pointer-events: none;
  }
  &__middle {
    background: var(--elka);
    padding-bottom: 20%;
    &__wrap {
      width: 260px;
      margin: 0 auto;
    }
    &__title {
      margin: 0 0 16px 0;
      span { color: var(--yellow); }
    }
    &__list {
      strong {
        display: block;
        color: var(--yellow);
        margin-bottom: 16px;
      }
      ul {
        margin: 32px 0 0 0;
        padding: 0;
        li {
          display: flex;
          align-items: center;
          list-style: none;
          font-size: 14px;
          color: #fff;
          margin-bottom: 12px;
        }
        i {
          background: var(--yellow);
          color: var(--green);
          width: 20px;
          height: 20px;
          font-style: normal;
          border-radius: 50%;
          font-feature-settings: "tnum";
          padding-left: 6px;
        }
        span {
          flex: 1;
          margin-left: 12px;
        }
      }
    }
    a {
      font-size: 14px;
      color: #fff;
      text-decoration: underline;
    }
  }
}
@media (max-width: 375px) {
  .elka {
    .elka__list {
      display: flex;
      flex-direction: column;
      gap: 6px;
      left: 55%;
    }
    .elka__text {
      h2 {
        font-size: 22px;
        margin: 0;
      }
      p {
        font-size: 16px;
        margin: 6px 0 0 0;
      }
    }
  }
}
</style>
