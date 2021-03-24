<template>
  <div id="tab_bar">
    <slot></slot>
  </div>
</template>

<script>
export default {
  name: "TabBar"
}
</script>

<style scoped>
  #tab_bar {
    display: flex;
    background-color: #f6f6f6;

    /*从顶部到底部*/
    position: fixed;
    left: 0;
    right: 0;
    bottom: 0;

    /*阴影*/
    box-shadow: 0 -1px 1px rgba(100, 100, 100, .2);
  }

</style>
