<template>
  <div class="mb-5 pb-5">
    <p class="text-center text-white mb-5 py-5 fs-lg-39">
      Benefit both ways - <em>monthly or yearly</em>
    </p>

    <div class="d-flex flex-column flex-lg-row mt-5">
      <ui-body-benefit-monthly-yearly />
      <ui-body-benefit-monthly-yearly
        title="Yearly"
        price="2.05"
        url="18%.svg"
        littlePrice="4.09"
        :bool="false"
      />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.fs-lg-39 {
  font-size: 30px;
  @include media-breakpoint-up(lg) {
    font-size: 39px;
  }
}
</style>
