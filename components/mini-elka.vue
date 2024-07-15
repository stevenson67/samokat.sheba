<template>
  <svg class="mini-elka" width="190" height="359" viewBox="0 0 190 359" fill="none" xmlns="http://www.w3.org/2000/svg">
    <g class="basis">
      <path fill-rule="evenodd" clip-rule="evenodd" d="M104.206 15.3149L156.6 167.33H136.377L187.344 333.799H111.706V358.815H92.7058V333.799H21.0674L72.0348 167.33H51.8113L104.206 15.3149Z" fill="#134B48"/>
      <path d="M75.0674 135.315C79.234 143.315 89.3674 153.815 96.5674 131.815" stroke="black" stroke-width="2"/>
      <path d="M129.067 133.776C125.191 141.687 115.765 152.069 109.067 130.315" stroke="black" stroke-width="2"/>
      <path d="M98.5674 152.815C96.0674 149.315 99.5674 143.315 103.067 143.315C107.067 143.315 113.067 145.315 109.567 151.315C106.067 157.315 101.067 156.315 98.5674 152.815Z" fill="#E73C5E"/>
      <path d="M94.5674 161.815C98.234 164.315 107.867 167.515 117.067 160.315" stroke="black" stroke-width="2"/>
      <circle class="blink" cx="83.8674" cy="59.6483" r="6.8" fill="#104643"/>
      <path class="blink" d="M85.91 71.2233C83.421 67.5728 86.9056 61.3148 90.3903 61.3148C94.3728 61.3148 100.346 63.4008 96.8618 69.6588C93.3771 75.9167 88.3991 74.8737 85.91 71.2233Z" fill="#E1A49E"/>
      <circle class="blink" cx="107.567" cy="73.8148" r="6.5" fill="#E73C5E"/>
      <path d="M127.067 68.8151C123.401 84.1484 110.821 116.923 89.0674 118.815C77.5674 119.815 82.3814 96.2088 89.5674 100.315C96.5674 104.315 70.5674 124.315 65.0674 112.815C60.6674 103.615 70.5674 94.6484 76.0674 91.3151" stroke="black" stroke-width="2"/>
      <path d="M150.067 201.315C141.288 218.612 106.197 252.261 36.0674 248.487" stroke="black" stroke-width="2"/>
      <circle class="blink" cx="140.633" cy="215.074" r="6.28966" fill="#EFDDA2"/>
      <circle class="blink" cx="104.467" cy="237.087" r="6.28966" fill="#E1A49E"/>
      <circle class="blink" cx="69.8743" cy="247.308" r="6.28966" fill="#D9D9D9"/>
      <path d="M40.0674 260.481C51.3111 282.632 96.2522 325.727 186.067 320.894" stroke="black" stroke-width="2"/>
      <circle class="blink" r="6" transform="matrix(-1 0 0 1 52.0674 278.315)" fill="#E1A49E"/>
      <circle class="blink" r="6" transform="matrix(-1 0 0 1 85.0674 301.315)" fill="#D9D9D9"/>
      <circle class="blink" r="6" transform="matrix(-1 0 0 1 36.0674 247.315)" fill="#D9D9D9"/>
      <circle class="blink" r="6" transform="matrix(-1 0 0 1 183.067 321.315)" fill="#EFDDA2"/>
      <circle class="blink" r="6" transform="matrix(-1 0 0 1 117.067 313.315)" fill="#E1A49E"/>
      <circle class="blink" r="6" transform="matrix(-1 0 0 1 153.067 321.315)" fill="#EFDDA2"/>
      <circle r="6" transform="matrix(-1 0 0 1 161.067 234.315)" fill="#104643"/>
    </g>
    <g class="waves">
      <path d="M174.273 158.444C173.667 166.21 171.509 173.913 168.993 181.261C168.978 181.305 167.642 185.286 167.642 183.492" stroke="black" stroke-width="2"/>
      <path d="M181.639 170.968C181.117 176.367 179.424 182.761 176.114 187.175" stroke="black" stroke-width="2"/>
    </g>
    <g class="waves">
      <path d="M11.0798 317.036C10.8719 319.064 10.3816 321.001 10.3112 323.06C10.2168 325.822 10.035 328.787 10.4184 331.533C10.7179 333.677 11.6541 335.919 13.4928 337.145" stroke="black" stroke-width="2"/>
      <path d="M1.01028 327.047C1.01028 326.103 0.987146 328.936 1.01028 329.88C1.08747 333.029 1.75065 336.156 3.29156 338.93C4.35427 340.843 6.29666 344.275 8.68139 344.871" stroke="black" stroke-width="2"/>
    </g>
    <g class="waves">
      <path d="M85.4183 23.8813C86.3336 20.3867 88.5564 17.066 90.83 14.3111C92.9772 11.7092 95.7057 9.31421 98.9837 8.31836C100.839 7.75487 102.63 7.70093 104.541 7.70093" stroke="black" stroke-width="2"/>
      <path d="M77.083 17.1804C77.6034 15.0514 79.1621 13.0339 80.4698 11.342C82.7654 8.37206 85.4577 5.59116 88.5963 3.50606C90.3144 2.36471 92.7476 1 94.8978 1" stroke="black" stroke-width="2"/>
    </g>
  </svg>
</template>

<script>
export default {
  name: "mini-elka"
}
</script>

<style lang="scss">
.mini-elka {
  .basis {
    transform-origin: center bottom;
    animation: .7s infinite ease-in-out shake;
  }
  .blink { animation: 1s infinite blink; }
  .waves { animation: .7s infinite ease-in-out waves; }
}
</style>
