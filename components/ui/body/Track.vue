<template>
  <div class="pt-5">
    <p class="text-center text-white fs-40 lh">
      Save Big on All Features <br />
      <span class="text-orange"> <em>no exceptions</em> </span>
    </p>
    <div class="track px-4 mt-5">
      <slider
        ref="slider"
        :options="options"
        class="mb-sm-5 ms-0 h-auto ps-4 ps-xxl-0 py-3"
      >
        <slider-item v-for="item of items" :key="item.url" class="mt-xxl-2">
          <div>
            <img
              :src="require(`/assets/images/body/track/${item.url}`)"
              alt=""
            />
            <br />
            <p class="text-size fs-20 text-white">{{ item.title }}</p>
          </div>
        </slider-item>
      </slider>

      <div class="bg-white mx-5 mt-5 size"></div>
      <div class="d-flex flex-column flex-lg-row text-white mt-3 padding">
        <div>
          <p class="fs-40">
            Track the time your employees spend on work and get detailed
            information
          </p>
          <div>
            <ul class="list-unstyled mt-5">
              <li>
                <img src="@/assets/images/body/done.svg" alt="" /> 4 Screenshot
                Modes
              </li>
              <li>
                <img src="@/assets/images/body/done.svg" alt="" /> Idle Time
                Tracking
              </li>
              <li>
                <img src="@/assets/images/body/done.svg" alt="" /> Synchronized
                Tracking
              </li>
              <li>
                <img src="@/assets/images/body/done.svg" alt="" /> Billable
                Hours
              </li>
            </ul>
          </div>
          <ui-button
            variant="primary"
            type="button"
            class="fw-bold btn-xl p-0 mt-3"
            text="RESERVE YOUR SEAT"
          />
        </div>

        <div class="text-center">
          <img
            src="@/assets/images/body/track/desk.svg"
            alt=""
            class="img-size"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [
        { title: "Time Tracking with Screenshots", url: "time.svg" },
        { title: "Productivity Monitoring", url: "man.svg" },
        { title: "Task Management", url: "task.svg" },
        { title: "Communication Channels", url: "comun.svg" },
        { title: "HR Tools", url: "hr.svg" },
        { title: "Online Reports", url: "online.svg" },
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
.fs-40 {
  font-size: 20px;
  @include media-breakpoint-up(lg) {
    font-size: 40px;
  }
}

.track {
  background-color: $body-color;
  border-radius: 26px;
}

.size {
  height: 2px;
  border-radius: 50px;
}

.padding {
  @include media-breakpoint-up(lg) {
    padding: 79px 54px 130px;
  }
}

.lh {
  line-height: 52px;
}

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

.fs-20 {
  font-size: 20px;
}

.text-size {
  padding: 0px 18px;
}

.img-size {
  width: 300px;
  @include media-breakpoint-up(xl) {
    width: auto;
  }
}
</style>
