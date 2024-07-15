<template>
  <section class="form">
    <div class="container">
      <h2 class="form__title">Подарки уже<br> упакованы, осталось<br> <span>зарегистрироваться</span></h2>
      <label>
        <input type="text" class="input" ref="code" v-model="code" placeholder="Введите код из смс"/>
      </label>
      <div class="button" @click="validate">Участвовать</div>
    </div>
<!--    <result v-if="resultView" :code="code" @close="resultView=false" @danger="danger"/>-->
    <result v-if="resultView" @close="resultView=false"/>
  </section>
</template>

<script>
import Result from "@/sections/result";
export default {
  name: "promo",
  components: {Result},
  data: ()=>({
    code: '',
    resultView: false,
  }),
  methods: {
    validate() {
      if (this.code) {
        this.$axios.$post(window.location.origin + '/query/', { code: this.code })
          .then(res => {
            if (res.code) {
              this.resultView = true;
            } else {
              this.danger()
            }
          })
      } else {
        this.danger()
      }
    },
    danger() {
      this.$refs.code.classList.add('danger')
      setTimeout(()=>{
        this.$refs.code.classList.remove('danger')
      }, 2000)
    }
  }
}
</script>

<style lang="scss">
.form {
  position: relative;
  z-index: 1;
  &__title {
    margin-bottom: 32px;
    span {
      color: var(--yellow);
    }
  }
  .button { margin: 0 auto; }
  .input { margin-bottom: 12px; }
}
</style>
