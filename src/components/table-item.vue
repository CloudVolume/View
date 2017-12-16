<template>
  <a class="m-table-item" :class="{'is-active':isActive}" @click="goToRouter">
    <span class="m-table-item-icon" v-show="!isActive"><slot name="icon-normal"></slot></span>
    <span class="m-table-item-icon" v-show="isActive"><slot name="icon-active"></slot></span>
    <span class="m-table-item-text"><slot></slot></span>
  </a>
</template>

<script>
  export default {
    props: {
      id: {
        type: String
      },
      isRouter: {
        type: Boolean,
        default: false
      }
    },
    computed: {
      isActive() {
        if (this.$parent.value === this.id) {
          return true
        }
      }
    },
    methods: {
      goToRouter() {
        this.$parent.$emit('input', this.id)
        //判断是否跳转路由
        if (this.isRouter) {
          //根据id跳转到对应的路由页面
          this.$router.push(this.id)
        }
      }
    }
  }
</script>
<style lang="less">
  @import "../assets/less/var.less";

  .m-table-item {
    flex: 1;
    text-align: center;
    .m-table-item-icon {
      display: block;
      padding-top: 2px;
      img {
        width: 28px;
        height: 28px;
      }
    }
    .m-table-item-text {
      display: block;
      font-size: 10px;
      color: #949494;
    }
    &.is-active {
      .m-table-item-text {
        color: @tableActiveColor
      }
    }
  }
</style>
