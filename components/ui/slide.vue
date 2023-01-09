<template>
  <div class="mt-5 py-5">
    <slider
      ref="slider"
      :options="options"
      class="mb-sm-5 ms-0 h-auto ps-4 ps-xxl-0 py-3"
    >
      <slider-item
        v-for="item of items"
        :key="item.logo"
        class="card-bg mt-xxl-2"
      >
        <img
          :src="require(`/assets/images/body/slider/${item.url}`)"
          class="card-logo logo-size mb-4 ms-4"
        />
      </slider-item>
    </slider>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { url: "product-1.svg" },
        { url: "product-2.svg" },
        { url: "product-3.svg" },
        { url: "product-8.svg" },
      ],

      options: {
        currentPage: 1,
        pagination: false,
        loop: true,
        slidesToScroll: 1,
        centeredSlides: true,
        autoplay: "1800",
        loopedSlides: 2,
        itemAnimation: true,
      },
    };
  },
};
</script>

<style lang="scss" scoped>
.slider {
  width: 25% !important;
  &-item {
    transition-timing-function: ease;
    transition-duration: 600ms;
    width: auto;
    display: block;
    color: $dark;
  }
}
</style>
