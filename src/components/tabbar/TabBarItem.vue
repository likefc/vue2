<template>
  <div class="tab-bar-item" @click="itemClick">
    <div v-if="!isActive">
      <slot name='item-icon'></slot>
    </div>
    <div v-else>
      <slot name='item-icon-active'></slot>
    </div>
    <div :class="{'active': isActive}">
      <slot name='item-text'></slot>
    </div>

    <!-- <div>
      <img src="../../assets/img/tabbar/home.svg" alt="">
    </div>
    <div>
      首页
    </div> -->
  </div>
</template>
<script>
export default {
  name: 'TabBarItem',
  data() {
    return {
      isActive: true
    }
  },
  props: {
    path: String
  },
  methods: {
    itemClick($event) {
      console.log($event)
      // if (this.path === this.$router)
      //  this.$router
      console.log(this.$router)
      console.log(this.$route.fullPath)
      this.$router.replace(this.path)
    }
  }
}
</script>
<style lang="css">
.tab-bar-item {
  flex: 1;
  text-align: center;
  font-size: 14px;
}
.tab-bar-item img {
  width: 24px;
  height: 24px;
  margin-top: 3px;
  vertical-align: middle;
}
.active {
  color: red;
}
</style>