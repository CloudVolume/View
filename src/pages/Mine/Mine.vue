<template>
<div>
  <m-header title="我的" fixed="">
    <a href="javascript:;" slot="right"><img class="m-icon-img margin-right-10" src="../../assets/images/ic_actionbar_search_icon.png" alt=""></a>
    <a href="javascript:;" slot="right"><img class="m-icon-img" src="../../assets/images/ic_chat_green.png" alt=""></a>

  </m-header>
</div>
</template>

<script>
  import mHeader from '../../components/header.vue'

  export default {
    name: 'mine',
    components: {
      mHeader
    }
  }
</script>

