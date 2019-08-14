<template>
  <i :class="classes"
     :style="styles"></i>
</template>
<script>
export default {
  props: {
    type: {
      type: String, //类型
      default: "", //默认
      required: true
    },
    size: {
      type: Number, //类型
      default: 12 //默认
    },
    color: {
      type: String,
      default: "red"
    }
  },
  computed: {
    classes() {
      return ["iconfont", `icon-${this.type}`];
    },
    styles() {
      return { fontSize: `${this.size}px`, color: `${this.color}` };
    }
  },
  data() {
    return {};
  }
};
</script>
<style lang='scss' scoped>
</style>