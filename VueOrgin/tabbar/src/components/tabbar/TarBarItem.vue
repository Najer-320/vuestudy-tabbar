<template>
  <div class="tab_bar_item" @click="itemClick">
    <div v-if="!isActive">
      <slot name="item_icon"></slot>
    </div>
    <div v-else>
      <slot name="item_icon_active"></slot>
    </div>
    <div :style="activeStyle">
      <slot name="item_text"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "TarBarItem",
  // 传入路径
  props: {
    path: String,
    // 动态更改颜色
    activeColor: {
      type: String,
      default: 'red'
    }
  },
  data() {
    return {
      // isActive: true,
    }
  },
  computed: {
    isActive() {
      // /home -> item1(/home) = true/false
      return this.$route.path.indexOf(this.path) !== -1
    },
    activeStyle() {
      return this.isActive ? {color: this.activeColor} : {}
    }
  },
  methods: {
    itemClick() {
      // console.log("itemClick")
      this.$router.replace(this.path)
    }
  }
}
</script>

<style scoped>
  .tab_bar_item {
    flex: 1;
    text-align: center;
    height: 49px;
    font-size: 12px;
  }

  .tab_bar_item img{
    width: 20px;
    height: 20px;
    margin-top: 5px;
    /*去除图片下面多余的三个像素*/
    vertical-align: middle;
  }

</style>
