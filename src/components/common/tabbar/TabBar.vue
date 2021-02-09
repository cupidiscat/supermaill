<template>
  <div class="tab-bar-wrap">
    <slot></slot>
  </div>
</template>

<script>
export default {
name: "TabBar"
}
</script>

<style scoped>
  .tab-bar-wrap {
    position: fixed;
    left: 0;
    bottom: 0;
    right: 0;

    height: 49px;
    font-size: 12px;

    background-color: #f2f2f2;
    box-shadow: 2px 2px 10px #ececec;

    display: flex;
  }
</style>
