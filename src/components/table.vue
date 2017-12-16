<template>
  <div class="m-table">
    <slot></slot>
  </div>
</template>

<script>
  import mTableItem from './table-item.vue'

  export default {
    props: ['value'],
    computed: {
    }
  }
</script>
<style lang="less">
  @import "../assets/less/var.less";

  .m-table {
    display: flex;
    flex-direction: row;
    position: fixed;
    bottom: 0;
    left: 0;
    right: 0;
    width: 100%;
    overflow: hidden;
    height: 50px;
    background: #fff;
    border-top: 1px solid #e4e4e4;
  }
</style>
