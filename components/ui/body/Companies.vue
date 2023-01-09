<template>
  <div class="my-5 py-5">
    <p class="text-center text-white fs-40">Trusted by 1000+ Companies</p>
    <div class="d-flex flex-wrap justify-content-around mt-5">
      <img
        v-for="item of items"
        :key="item.url"
        :src="require(`/assets/images/body/companies/${item.url}`)"
        alt=""
      />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { url: "logo1.svg" },
        { url: "logo2.svg" },
        { url: "logo3.svg" },
        { url: "logo4.svg" },
        { url: "logo5.svg" },
        { url: "logo6.svg" },
        { url: "logo7.svg" },
        { url: "logo8.svg" },
        { url: "logo9.svg" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.fs-40 {
  font-size: 20px;
  @include media-breakpoint-up(lg) {
    font-size: 40px;
  }
}
</style>
