<template>
  <button class="btn" :class="classes" :type="type" :disabled="disabled">
    <span
      v-if="variant === 'outline-primary'"
      class="text-gradient"
      :class="{ 'text-gradient-disabled': disabled }"
    >
      {{ text }}
    </span>
    <slot v-else>{{ text }}</slot>
  </button>
</template>

<script>
export default {
  props: {
    variant: {
      type: String,
      default: () => "",
    },
    type: {
      type: String,
      default: () => "submit",
    },
    size: {
      type: String,
      default: () => null,
    },
    block: {
      type: Boolean,
      default: () => false,
    },
    text: {
      type: String,
      default: () => "",
    },
    disabled: {
      type: Boolean,
      default: false,
    },
  },
  computed: {
    classes() {
      let res = [`btn-${this.variant}`];
      if (this.variant === "") {
        res = [];
      }
      if (this.size) {
        res.push(`btn-${this.size}`);
      }
      if (this.block) {
        res.push("btn-block");
      }
      return res;
    },
  },
};
</script>
