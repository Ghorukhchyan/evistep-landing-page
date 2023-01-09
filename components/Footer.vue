<template>
  <div class="py footer text-white">
    <div class="text-sm-left">
      <p class="fs-49">Save 50% Now</p>
      <ui-button
        variant="primary"
        type="button"
        class="fw-bold btn-xl p-0 mt-3"
        text="GET MY DISCOUNT"
      />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.footer {
  background-color: $body-color;
  position: relative;

  background-image: url("@/assets/images/footer/background.svg"),
    url("@/assets/images/footer/ellipse-left-middle.svg"),
    url("@/assets/images/footer/ellipse-left-top.svg"),
    url("@/assets/images/footer/ellipse-right-top-first.svg"),
    url("@/assets/images/footer/ellipse-right-top-second.svg");
  background-position: 100% 34%, 82% 74%, 70% 100%, 97% 28%, 92% 33%;
  background-size: auto, auto, auto, auto, auto, auto;
  background-repeat: no-repeat;
}
.fs-49 {
  font-size: 25px;
  @include media-breakpoint-up(lg) {
    font-size: 49px;
  }
}

.py {
  padding: 50px;
  @include media-breakpoint-up(lg) {
    padding: 135px;
  }
}

.text-sm-left {
  text-align: center;
  @include media-breakpoint-up(md) {
    text-align: left;
  }
}
</style>
