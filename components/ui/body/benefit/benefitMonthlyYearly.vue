<template>
  <div class="card-width">
    <div class="card card-benefit h-100 border-0 rounded-5 rounded-sm-6">
      <div
        class="card-header d-flex flex-row justify-content-center align-items-center text-dark bg-transparent"
      >
        <h3 class="mb-0 fs-inherit mt-4 fs-40 fw-bolder text-white">
          {{ title }}
        </h3>
        <img
          :src="require(`/assets/images/body/${url}`)"
          class="position-absolute position w-150"
        />
      </div>

      <div class="text-center">
        <p class="fw-bolder fs-lg-80">
          <img
            src="@/assets/images/body/dell.svg"
            alt=""
            class="position-absolute dell-pos"
          />
          <span class="fs-30 fw-bold position-absolute span-pos"
            >${{ littlePrice }}</span
          >
          ${{ price }}
        </p>
        <h5>per user/month</h5>
        <div class="d-flex flex-column m-auto align-items-start mw-200">
          <div
            v-for="(item, i) in items"
            :key="i"
            class="d-flex justify-content-center mt-4"
          >
            <img src="@/assets/images/body/done.svg" alt="" />
            <p class="m-0">{{ item.text }}</p>
          </div>
        </div>
      </div>

      <div class="text-center w-100 mt-5 mb-3">
        <ui-button
          variant="primary"
          type="button"
          class="fw-bold btn-xl p-0"
          text="GET YOUR DEAL"
        />
        <p class="text-end" v-if="bool">*for 6 months</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          text: "14-day Free Trial",
        },
        {
          text: "Access to All Features",
        },
        {
          text: "24/7 Support",
        },
      ],
    };
  },
  props: {
    title: {
      type: String,
      default: () => "Monthly",
    },
    url: {
      type: String,
      default: () => "50%.svg",
    },
    price: {
      type: [Number, String],
      default: () => 2.49,
    },
    littlePrice: {
      type: [Number, String],
      default: () => 4.99,
    },
    bool: {
      type: Boolean,
      default: () => true,
    },
  },
};
</script>

<style lang="scss" scoped>
.mw-200 {
  max-width: 200px;
}

.w-150 {
  width: 150px;
  @include media-breakpoint-up(lg) {
    width: 180px;
  }
  @include media-breakpoint-up(xl) {
    width: auto;
  }
}

.position {
  left: 60%;
  bottom: 36px;
  @include media-breakpoint-up(sm) {
    left: 83%;
    bottom: 36px;
  }
  @include media-breakpoint-up(lg) {
    left: 68%;
    bottom: 33px;
  }
  @include media-breakpoint-up(xl) {
    left: 60%;
    bottom: -40px;
  }
}
.span-pos {
  right: 70%;
}

.dell-pos {
  left: 42px;
  top: 125px;
  z-index: 1;
  @include media-breakpoint-up(md) {
    left: 91px;
    top: 146px;
  }
  @include media-breakpoint-up(lg) {
    left: 77px;
    top: 150px;
  }
}

.card-header {
  position: relative;
  padding: 14px 0px 22px;
  @include media-breakpoint-up(sm) {
    padding: 24px 0 32px;
  }
}
</style>
