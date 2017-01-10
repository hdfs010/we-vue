<template>
  <header class="wv-header" :class="{ 'is-fixed': fixed }">
    <div class="left">
      <slot name="left"></slot>
    </div>
    <h1 class="wv-header-title" v-text="title"></h1>
    <div class="wv-header-button">
      <slot name="right"></slot>
    </div>
  </header>
</template>

<script type="text/babel">
export default {
  name: 'wv-header',

  props: {
    title: String,
    skin: {
      type: String,
      default: 'ios'
    },
    fixed: {
      type: Boolean,
      default: true
    }
  }
}
</script>

<style scoped lang="scss">
  .wv-header {
    display: block;
    overflow: hidden;
    background-color: #21292c;
    width: 100%;
    height: 50px;
    padding: 0;
    margin: 0;
    color: white;
    font-size: 14px;

    .wv-header-title {
      margin: 0;
      padding: 0;
      line-height: 50px;
      font-weight: 100;
    }

    &.is-fixed {
      position: fixed;
      left: 0;
      top: 0;
    }
  }
</style>
