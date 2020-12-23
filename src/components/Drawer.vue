<template>
  <div id="drawer">
    <div class="not-collapse-content" @click="changeActive">未折叠内容</div>
    <div :class="active?'collapse-content active':'collapse-content'">折叠内容</div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      active: false
    }
  },
  methods: {
    changeActive() {
      this.active = !this.active;
    }
  }
}
</script>

<style lang="scss" scoped>
#drawer {
  width: 500px;
  height: auto;
  border: 1px solid #ccc;
  .not-collapse-content {
    font-size: 100px;
  }
  .collapse-content {
    font-size: 100px;
    transform: scaleY(0);    
    transform-origin: top;
    transition: transform 0.26s ease;
    height: 0px;
    &.active {
      transform: scaleY(1);
      height: auto;
    }
  }
}
</style>