<template>
  <div
    class="d-flex flex-column flex-lg-row justify-content-between mt-4 pt-2 pt-lg-5 mb-5"
  >
    <div>
      <p class="fs-2 fs-lg-50 text-orange pe-320">
        CYBER MONDAY <span class="text-white">means an even</span> BIGGER SALE
      </p>
      <h6 class="pb-lg-4 pb-3 pe-320">
        Cyber Monday saves you money, WebWork saves you time.
      </h6>
      <ui-button
        variant="primary"
        type="button"
        class="fw-bold btn-xl p-0"
        text="SAVE BIG NOW"
      />
      <p class="pt-2">
        <img src="@/assets/images/body/Check.svg" alt="" />
        <span>14-day free trial No credit card required</span>
      </p>
      <p class="pt-5 pt-lg-4">
        <img src="@/assets/images/body/Stars.svg" alt="" />
        <span>Reviews from 51K+ happy users below and beyond</span>
      </p>
      <img src="@/assets/images/body/app1.svg" alt="" />
      <img src="@/assets/images/body/app2.svg" alt="" />
      <img src="@/assets/images/body/app3.svg" alt="" />
    </div>
    <div class="align-self-center">
      <img src="@/assets/images/body/Count.svg" alt="" class="width" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.fs-lg-50 {
  @include media-breakpoint-up(lg) {
    font-size: 50px;
  }
}

.width {
  width: 350px;
  @include media-breakpoint-up(sm) {
    width: 500px;
  }
  @include media-breakpoint-up(lg) {
    width: auto;
  }
}

.pe-320 {
  @include media-breakpoint-up(xxxl) {
    padding-right: 320px;
  }
}
</style>
