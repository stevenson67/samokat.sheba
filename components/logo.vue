<template>
  <svg width="226" height="56" viewBox="0 0 226 56" fill="none" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
    <rect y="12.5" width="107" height="31" fill="url(#pattern01)"/>
    <path d="M128 17L128 39" stroke="#969696" stroke-linecap="round"/>
    <rect x="149" width="77" height="56" fill="url(#pattern11)"/>
    <defs>
      <pattern id="pattern01" patternContentUnits="objectBoundingBox" width="1" height="1">
        <use xlink:href="#image01_173_476" transform="matrix(0.00028943 0 0 0.000999001 -0.00158253 0)"/>
      </pattern>
      <pattern id="pattern11" patternContentUnits="objectBoundingBox" width="1" height="1">
        <use xlink:href="#image11_173_476" transform="matrix(0.000840778 0 0 0.00115607 -0.00446663 0)"/>
      </pattern>
      <image id="image01_173_476" width="3466" height="1001" href="../static/media/logo/logo-samokat.png"/>
      <image id="image11_173_476" width="1200" height="865" href="../static/media/logo/logo-sheba.png"/>
    </defs>
  </svg>
</template>

<script>
export default {
  name: "logo",
  props: {
    color: {
      type: String,
      default: 'var(--coral)'
    }
  }
}
</script>

<style lang="scss">

</style>
