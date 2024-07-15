<template>
  <main class="main">
    <cookies/>
    <hero/>
    <elka/>
    <promo/>
    <apps/>
    <footr/>
  </main>
</template>

<script>
import Hero from "~/sections/hero";
import Elka from "~/sections/elka";
import Promo from "@/sections/promo";
import Apps from "@/sections/apps";
import Footr from "@/sections/footr";
import Cookies from "@/components/cookies";
export default {
  components: {Cookies, Footr, Apps, Promo, Elka, Hero},
  methods: {
    scrollToForm() {
      let form = document.querySelector('.form')
      window.scroll({
        behavior: 'smooth', left: 0,
        top: form.offsetTop - window.innerHeight / 4
      });
    }
  },
  mounted() {
    document.addEventListener('scroll', function () {
      let offset = window.scrollY - window.innerHeight / 100

      document.querySelectorAll('svg path.scroll-1').forEach(item => {
        item.style = `transform: translateY(${offset/4}px)`
      })
      document.querySelectorAll('svg path.scroll-2').forEach(item => {
        item.style = `transform: translateY(${offset/3.5}px)`
      })
      document.querySelectorAll('svg path.scroll-3').forEach(item => {
        item.style = `transform: translateY(${offset/2}px)`
      })
      document.querySelectorAll('svg path.scroll-4').forEach(item => {
        item.style = `transform: translateY(${offset/1.5}px)`
      })
      document.querySelectorAll('svg path.scroll-h').forEach(item => {
        item.style = `transform: rotate(${offset/20}deg)`
      })
      document.querySelectorAll('svg path.scroll-hi').forEach(item => {
        item.style = `transform: rotate(-${offset/20}deg)`
      })

      document.querySelectorAll('svg path.scroll-light').forEach(item => {
        let bound = item.getBoundingClientRect()
        if (bound.top < window.innerHeight/1.75)
          item.classList.add('active')
        else
          item.classList.remove('active')
      })
    })

    document.querySelectorAll('.button.start').forEach(item => {
      item.addEventListener('click', this.scrollToForm)
      item.addEventListener('touchend', this.scrollToForm)
    })
  }
}
</script>
