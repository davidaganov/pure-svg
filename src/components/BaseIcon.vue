<template>
  <svg
    :width="sizes ? sizes : width"
    :height="sizes ? sizes : height"
    :aria-labelledby="name"
    :style="rotate ? `transform: rotate(${rotate}deg)` : undefined"
    :viewBox="box"
    role="presentation"
  >
    <title
      v-if="name"
      lang="en"
    >
      {{ name }}
    </title>

    <g
      :fill="stroke === false ? color : 'none'"
      :stroke="stroke ? color : 'none'"
    >
      <slot />
    </g>
  </svg>
</template>

<script>
export default {
  props: {
    name: { type: String, default: undefined },
    color: { type: String, default: "currentColor" },
    stroke: { type: Boolean, default: false },
    width: { type: Number, default: 18 },
    height: { type: Number, default: 18 },
    sizes: { type: Number, default: NaN },
    box: { type: String, default: "0 0 18 18" },
    rotate: { type: Number, default: NaN }
  }
}
</script>
